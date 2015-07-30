# Compile LESS using Node

[← Go back to LESS overview](https://github.com/heyallan/less-pocket)

*Prerequisites:*
- Node: https://github.com/heyallan/node
- NPM (comes with Node)

*Pros:*
- Easiest and fastest way to get started
- You'll only need command line

*Cons:*
- Little to no options
- Zero automatization

## Example

### Compile
```shell
## install less compiler globally
$ npm install -g less

## go to project
## if you don't know the exact path to project, you can copy the folder from finder and paste it into command line
$ cd path/to/project/

## compile less
$ lessc --compress ./src/styles.less > ./dist/styles.min.css
```

*Source: http://lesscss.org/usage/#command-line-usage*

### Before compilation

```
project/
├── src/
│   ├── less/
│   │   ├── styles.less
│── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── <empty>
```

### After compilation
```
project/
├── src/
│   ├── less/
│   │   ├── styles.less
├── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── styles.min.css
```
Rinse and repeat.
