# `@themaxdavitt/hastscript-components`

Wrap [`hastscript`](https://www.npmjs.com/package/hastscript) to allow function pseudo-components

## Install

```
npm install --save hastscript @themaxdavitt/hastscript-components
```

## Usage

Pretend this is JSX, not the underlying transpiled calls.

```js
import { jsx } from '@themaxdavitt/hastscript-components';

// Async functions are also supported
function Hello({ children, greeting }) {
	return jsx('p', { children: [greeting, ' ', ...children, '!'] });
}

// <Hello greeting="Hello">Max</Hello> => <p>Hello Max!</p>
console.log(await jsx(Hello, { children: ['Max'], greeting: 'Hello' }));

// <p>Hello world!</p>
console.log(await jsx('p', { children: ['Hello world!'] }));
```

## License

MIT License, see [`LICENSE`](LICENSE).
