
### `Intro`
![GitHub Actions status | linter](https://github.com/anzerr/promise.util/workflows/linter/badge.svg)
![GitHub Actions status | publish](https://github.com/anzerr/promise.util/workflows/publish/badge.svg)
![GitHub Actions status | test](https://github.com/anzerr/promise.util/workflows/test/badge.svg)

simple es6 promise util.

#### `Install`
``` bash
npm install --save git+https://git@github.com/Product-Live/promise.util.git
```

### `Example`
``` javascript
const promise = require('@product-live/promise.util');
const data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

promise.measure(() => {
	return promise.each(data, () => promise.delay(1000), 5);
}).then((res) => {
	console.log(Math.round(res / 1e9)) // 2
});
```