# CSS Modules: Search paths to resolve compose directives

With this config:

```javascript
{
  'paths': [ 'src/style', 'components/style' ]
}
```

given two files: 'src/style/base.css' and 'components/style/button.css:

```css
.myClass {
  composes: button from "button.css";
  color: green;
}
```

into:

```css
.myClass {
  composes: button from "components/style/button.css";
  color: green;
}
```

## Options

- _paths_ - array of search paths

## Building

```
npm install
npm build
npm test
```

## Development

- `npm watch` will watch `src` for changes and rebuild
- `npm autotest` will watch `src` and `test` for changes and retest

## License

MIT
