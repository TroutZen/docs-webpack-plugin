# docs-webpack-plugin
A webpack plugin for validating documentation and generating a json file representing your class' documentation

## usage
```Javascript
var DocsPlugin = require('docs-webpack-plugin');

module.exports = {
    plugins: [
        new DocsPlugin({
            file: 'static/docs.json'
        })
    ]
};
```

## cli
To aid in automated linting of your documentation, there is also a cli format under ```$(npm bin)/docs-cli```.
Run it with no parameters for information about the interface.

## format
reading the dsl specification is a bit of a chore, so make a comment on top of each of your classes that looks a little like this:
```Javascript
/**\

    title: MyComponent
    category: component
    description: A super sweet component for making interfaces
    props:
        label[String]: What shows up on top
        onClick: What gets called on a click

\**/
```
