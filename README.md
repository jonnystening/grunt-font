grunt-font
==========

> Add soothing sound notification to your grunt watch so you don't need to watch the watch.

[![NPM](https://nodei.co/npm/grunt-font.png)](https://nodei.co/npm/grunt-font/)

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide,
as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins.
Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-font --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-font');
```

## The "font" task

### Overview
In your project's Gruntfile, add a section named `font` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
	font: {
		start: {
			text: "Welcome",
		},
	},
});
```


### Supported Characters

- A
- B
- C
- D
- E
- F
- G
- H
- I
- J
- K
- L
- M
- N
- O
- P
- Q
- R
- S
- T
- U
- V
- W
- X
- Y
- Z
- 0
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9
- !
- ?
- .
- +
- -
- _
- =
- @
- #
- $
- %
- &
- (
- )
- /
- :
- ;
- ` ` (space)


### Options


#### options.font
Type: `String`  
Default value: `block`

This is the font face you want to use. So far this plugin ships with with following font faces:

* block [colors: 2]


#### options.colors
Type: `Array`  
Default value: `[]`

In this setting you can set the colors for each font face. Use the color strings build in by [chalk](https://github.com/sindresorhus/chalk):

- `black`
- `red`
- `green`
- `yellow`
- `blue`
- `magenta`
- `cyan`
- `white`
- `gray`


#### options.background
Type: `string`  
Default value: `Black`

In this setting you can set the background colors for the output. Use the color strings build in by [chalk](https://github.com/sindresorhus/chalk):

- `Black`
- `Red`
- `Green`
- `Yellow`
- `Blue`
- `Magenta`
- `Cyan`
- `White`


#### options.space
Type: `Boolen`  
Default value: `true`

Set this option to false if you don't want the plugin to insert two empty line on top and on the bottom of the output.


#### options.maxLength
Type: `Integer`  
Default value: `10`

This option sets the maximum characters that will be printed on one line. As the shell usually don't give you access to its width this is nessesary
to not end up with a scrambled text output.


### Usage Examples

#### Default Options
In this example, the default options are used which will print your text in block and white.

```js
font: {
	start: {
		options: {
			font: 'block', //define the font face
			colors: [], //define all colors
			background: 'Black', //define the background color
			space: true, //define if the output text should have empty lines on top and on the bottom
			maxLength: 10
		},
		text: "Welcome",
	},
},
```

#### Custom Options
Choose different colors:

```js
font: {
	start: {
		text: "Welcome",
		option: {
			colors: ["black", "blue"],
			background: 'cyan',
		},
	},
},
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style.
Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
* 0.0.2 - path fixes
* 0.0.1 - alpha test

## License
Copyright (c) 2014 Dominik Wilkowski. Licensed under the [MIT license](https://github.com/dominikwilkowski/grunt-font/blob/master/LICENSE-MIT).