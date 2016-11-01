# grid-breakpoint [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]
> grid auto add breaking-point

## Installation

```sh
$ npm install --save grid-breakpoint
```

## Usage

```js
import React, {Component} from 'react';
import GridBreakPoint from 'grid-breakpoint';

class GridExample extends Component {
	render() {
    const list = range(20).map((col, i) => {
      return <div key={i}>{col}</div>;
    });

		return (
			<GridBreakpoint lg={4} md={3} xs={6}
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
