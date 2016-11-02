# grid-breakpoint [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]
> grid auto add breaking-point

## Installation

```sh
$ npm install --save grid-breakpoint
```

## Problem

Grid is great! But one big problem in grid is when you have a list of grid, and it's height is different, your grid will break easily.

`grid-breakpoint` automatically calculate and wrapped `Row` for `Col`!

## Usage

**IMPORTANT NOTE:** You need to use `webpack` as build tool, cause the grid system is based on [react-flexbox-grid](https://github.com/roylee0704/react-flexbox-grid), it'll load [flexboxgrid](https://github.com/kristoferjoseph/flexboxgrid) via `style-loader` and `css-loader` make sure you installed both of them.

```js
import React, {Component} from 'react';
import GridBreakPoint from 'grid-breakpoint';

class GridExample extends Component {
  render() {
    const list = range(20).map((col, i) => {
      return <div key={i}>{col}</div>;
    });

    // in this example, when the screen width is large(lg)
    // it'll wrap <Col/> as structure below
    // <Row> ---> automaticlly wrapped
    //   <Col/>
    //   <Col/>
    //   <Col/>
    // </Row>

    // in md screen
    // <Row> ---> automaticlly wrapped
    //   <Col/>
    //   <Col/>
    // </Row>

    // in xs screen (xs + xsOffset = 6)
    // <Row> ---> automaticlly wrapped
    //   <Col/>
    //   <Col/>
    // </Row>

    return (
      <GridBreakpoint lg={4} md={6} xs={3} xsOffset={3}
        rowClassName="row-test" colClassName="col-test">
        {list}
      </GridBreakpoint>
    );
  }
}

```

## Start example server

```
node devServer.js
```

## License

MIT © [Canner](https://github.com/canner)


[npm-image]: https://badge.fury.io/js/grid-breakpoint.svg
[npm-url]: https://npmjs.org/package/grid-breakpoint
[travis-image]: https://travis-ci.org/Canner/grid-breakpoint.svg?branch=master
[travis-url]: https://travis-ci.org/Canner/grid-breakpoint
[daviddm-image]: https://david-dm.org/Canner/grid-breakpoint.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/Canner/grid-breakpoint
