# Compile LESS using Node

- Requires Node: https://github.com/heyallan/node
- Requires NPM (comes with Node)

Compiling LESS with Node is the easiest and fastest way to get started because you only need command line, but it also offers few options and zero automatization, and software is supposed to be all about automatization.

## Node example

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
