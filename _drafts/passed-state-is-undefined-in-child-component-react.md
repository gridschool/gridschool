---
layout: post
tags:
- react
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Passed state is undefined in child component React
abstract: This is why your props could be undefined in a child component in React.
img_url: "/uploads/1200px-react-icon-svg.png"
date: 2021-01-13 07:00:00 +0000

---
## Undefined props in your child component.

One of the reasons that it gets undefined is because props are not being passed consistently in both components, heres why:

Let's say you have a functional component that looks like this:

    ...
    const Product = (props) => (
      <div className="ProductItem">
        <h2>{props.product.title}</h2>
        <p>{props.product.price}</p>
        {props.imported ? <button>Add to import list</button> : ""}
      </div>
    );
    
    export default Product;
    

Then you import that component into two different components.

Component one:

In this component you pass the **imported** prop

    ...
    class ImportList extends Component {
      render() {
        return (
          <div className="ImportListContainer">
            <h2>Products to import</h2>
            <Product imported={true} />
          </div>
        );
      }
    }
    
    export default ImportList;
    

Component two:

In this component you pass the **product** prop which would be an entire object

    ...
    class Products extends Component {
      render() {
        const productsList = this.props.prodLst.map((product) => {
          return (
            <Product key={product.id} product={product} />
          );
        });
        return (
          <div className="ProductsContainer">
            <h2>Products list</h2>
            {productsList}
          </div>
        );
      }
    }
    
    const mapStateToProps = (state) => {
      return {
        prodLst: state.prodLst.products,
      };
    };
    
    export default connect(mapStateToProps, null)(Products);
    

So if you are consistent with the props you pass to your child component it won't get undefined.