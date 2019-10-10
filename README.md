# Code saple for using Next.js with Preact

* [Next.js](https://nextjs.org/)
* [Preact](https://preactjs.com/)

The key is here in `next.config.js`:

```js
// next.config.js
module.exports = {
    // ...
    webpack: (config, options) => {
        config.resolve.alias = Object.assign({}, config.resolve.alias, {
            react: 'preact/compat',
            'react-dom/test-utils': 'preact/test-utils',
            'react-dom': 'preact/compat',
        });

        return config;
    },
    // ...
};
```
