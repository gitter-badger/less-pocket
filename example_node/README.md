# Compile LESS using Node

[← Go back to LESS overview](https://github.com/heyallan/less-pocket)

Prerequisites:
- Node (see [Node Pocket Guide](https://github.com/heyallan/node-pocket))
- NPM (comes with Node, see [NPM Pocket Guide](https://github.com/heyallan/npm-pocket))

Pros:
- Easiest and fastest way to get started
- You'll only need command line

Cons:
- Little to no options
- Zero automatization

## Example

### Compile
```shell
## install less compiler globally
$ npm install --global less

## compile less
$ lessc --compress ./src/styles.less > ./dist/styles.min.css
```

*Source: http://lesscss.org/usage/#command-line-usage*

### Before compilation

```
project/
├── package.js
├── gulpfile.js
├── src/
│   ├── less/
│   │   ├── styles.less
│── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── <-- empty
```

### After compilation
```
project/
├── package.js
├── gulpfile.js
├── src/
│   ├── less/
│   │   ├── styles.less
├── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── styles.css <-- compiled file
```
