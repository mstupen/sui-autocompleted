# SUI-Autocompleted

React component that shows a list of suggestions under an input file when you start to write something.
It's based on the container component design ( [more info](https://medium.com/@learnreact/container-components-c0e67432e005) ).

## Demo page

Checkout a Sui-Autocompleted component demo [here](http://sui-components.github.io/sui-autocompleted/).

## Usage

The component exposes the following props:

* placeholder (String): **Optional** Default text value for the input file when no key is pressed (placeholder value).
* suggests (Array): **Required** Array of SuggestionObjects. Te array contains the suggestions to show. If you don't want to show anything you have to send an empty array.
* handleChange (Function): **Required** This function is called everytime user change the input field value.

	```javascript
		const handleChange = function( inputFileValue ){ ... }
	```
* handleSelect (Function): **Required** This function is called when one suggestion is selected (via click or enter pressed).

	```javascript
		const handleSelect = function( suggestionValue ){ ... }
	```

and then you have to create containers which one setting that properties in the sui-autocompleted component. You can view an example of this kind of container in the [doc folder](https://github.com/scm-spain/sui-autocompleted/blob/master/docs/autocompleted-container.jsx).

### SuggestObject

An SuggestObject is a plain JS Object with these specials keys:

```javascript
{
    'id': [Unique id for the suggestion],
    'value': [value to be passed to the handleSelect callback function]
    'content': [React Component] or [Text to be show in the UI]
    'literal': [String] This key is REQUIRED only if you are using a ReactJS Component like a content. It is used to decide which text has to be put in the input text when this suggestion is selected, in other case content will be used,    
}
```

### Theme

There are several classes in order to apply a theme to the component:

* sui-autocompleted
* sui-autocompleted-input
* sui-autocompleted-clear
* sui-autocompleted-results
* sui-autocompleted-item
* sui-autocompleted-item--active

The component exports a basic CSS that you can include from the package in the node_modules.

## Installation

In order of running the source code and start playing with the examples:

* `$ git clone https://github.com/scm-spain/sui-autocompleted`
* `$ cd sui-autocompleted`
* `$ npm install`
* `$ npm run dev`
*  Go to _localhost:8080_


## Testing
Execute a complete test by running:

```
There are two options for executing tests:

* Single mode: `$ npm test`
* Watch mode: `$ npm run test:watch`

```
In addition, you can run specific test for linting JS and SASS:
SASS: (SASS linting rules specified in file `.scss-lint.yml`)

```
$ npm run lint:sass
```

## NPM
- The SUI-Card component is available as a NPM package [here](https://www.npmjs.com/package/@schibstedspain/sui-autocompleted):
```
npm install @schibstedspain/sui-autocompleted`
```

##ToDo


