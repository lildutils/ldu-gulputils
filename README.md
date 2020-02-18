# ldu-gulputils

## BuildUtils

Build Utilities for easy manage Gulpfile.js build tasks, you can import it in your Gulpfile.js

```js
const buildUtils = require('ldu-gulputils').buildUtils;
```

### generateHash

It generates a unique hash string with given length

```js
console.log(buildUtils.generateHash(16));
// output: generated hash with 16 length
// NOTE: the default hash length is 8
```

### getActiveProfile

It returns the value from the --p={activeProfile} argument

```js
console.log(buildUtils.getActiveProfile());
// output: 'dev'
// NOTE: if running gulp --p=dev
```

### getBuildName

It returns a formatted .zip file name for builds by given project informations

```js
console.log(buildUtils.getBuildName('project-name', '1.0.0-SNAPSHOT'));
// output: project-name-1.0.0-SNAPSHOT-yyyymmddHHMMss.zip
```

### getUsername

It returns the value of your username on your operating system

```js
console.log(buildUtils.getUsername());
// output: %USERNAME% | $USER
```

### mergeJSON

It merges the given source JSON objects into one JSON object

```js
console.log(buildUtils.mergeJSON(
    {"hello": "hello", "number": 1},
    {"hello": "world"}
));
// output: { "hello": "world", "number": 1 }
```

### processPackageFile

Copies the given properties from the given package.json file to a new processed object

```js
console.log(buildUtils.processPackageFile(packageJSON, 'hello'));
// output: { "hello": value of packageJSON.hello }
```

### processPHPContent

Concatenate the given content from .php files into one processed string value

```js
console.log(buildUtils.processPHPContent('<?php echo "hello world";?><?php echo php_info();?>'));
// output: '<?php echo "hello world"; echo php_info();?>'
```

## DateUtils

Date Utilities for easy handle date in Gulpfile.js tasks, you can import it in your Gulpfile.js

```js
const dateUtils = require('ldu-gulputils').dateUtils;
```

### getNow

Gets the now as Date

```js
console.log(dateUtils.getNow());
// output: now Date
```

### getNowFormatted

Gets the formatted now as string

```js
console.log(dateUtils.getNowFormatted());
// output: now string in yyyymmddHHMMss format
```

## Development

### Install

```sh
npm install
```

### Build

If you want to build the source code, you should run:

```sh
gulp build
```

## About

To get more informations about this project, or if you have any question or suggestion, please send an email to [me](mailto:lildworks@gmail.com)

## 

Thanks :)