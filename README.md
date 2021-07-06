
# Fabric React Components

​Use this collection of reusable React components to build your own custom commerce UI with [Fabric  APIs](https://docs.fabric.inc/api/). You can use these React components with [Fabric XM](https://fabric.inc/xm) or any another headless CMS.

## What is Fabric?

​[Fabric](https://fabric.inc/) is a [headless commerce](https://resources.fabric.inc/blog/glossary/headless-commerce) platform that lets you scale commerce across infinite channels with [commerce APIs](https://fabric.inc/ecommerce-apis), a [headless CMS](https://fabric.inc/xm), and cloud-native [commerce modules](https://fabric.inc/products). Build enterprise-grade solutions using the languages and tools you already love.

## Get Started 

​To get started with Fabric React components, you need to install them and get the credentials that let you perform the API calls they wrap. 

-  [Installation](#installation)
-  [Import](#import)

### Installation

Fabric React components are available as an [npm  package](https://www.npmjs.com/package/@fabric/react-components):

```
// npm
npm install @fabric/react-components

// yarn
yarn add @fabric/react-components
```

### Import

​You can use an ES6-named import with each component you want to use, in addition to the `fabric` component as follows:

```
import { fabric, ...otherComponents } from '@fabric/react-components'
```

Check [this  summary  table](#list-of-components) for the complete list of available components.

## Usage

​The following code snippets show you how to use Fabric React components in common scenarios. Check the [`pages`](/pages) folder of this repository for more detailed examples.

-  [Product  information](#product-information)
-  [Shopping  cart](#shopping-cart)
-  [Cart  summary](#cart-summary)

### Product  information

​This example uses Fabric React components to show product information:

```
import {
  fabric,
  PricesContainer,
  Price
} from '@fabric/react-components'

// your code [...]

<ProductContainer>
    <PI
      className="your-custom-class"
    />
    <PI
      className="your-custom-class"
    />
    <PI
      className="your-custom-class"
    />
  </ProductContainer>

// your code [...]
```

### Shopping  cart

​This example uses Fabric React components to build a shopping cart UI containing items that will be purchased, along with their information (image, name, quantity, price) and the option to remove items from the cart:

```
import {
  OrderStorage
  shoppingCart
  Errors
} from '@fabric/react-components'

// your code [...]

      <OrderContainer>
        <LineItemsContainer>
          <p className="your-custom-class">
            Your shopping cart contains <LineItemsCount /> items
          </p>
          <LineItem>
            <LineItemImage width={50} />
            <LineItemName />
            <LineItemQuantity max={10} />
            <Errors resource="lineItem" field="quantity" />
            <LineItemAmount />
          </LineItem>
        </LineItemsContainer>
      </OrderContainer>

// your code [...]

```

The `Errors` component lets you show any errors returned by the Fabric API on a single attribute of a specific item. You can customize the error message by passing the `messages` prop to the component.

### Cart  summary

​This example uses Fabric React components to show a sample order summary with all the order line items including discounts, shipping costs, taxes, gift cards (if present) and totals:



##  Contributing

​We welcome contributions to this repository and other open source projects from Fabric. You can open pull requests and view [CONTRIBUTING.md](./CONTRIBUTING.md) for commit formatting details.

## License

​This repository is published under the [MIT](LICENSE) license.

## Code  of  Conduct

​This project adheres to the [Fabric  Community  Guidelines](./CODE_OF_CONDUCT.md). By participating, you are expected to honor these guidelines.
