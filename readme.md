# gifsicle-bin ![GitHub Actions Status](https://github.com/imagemin/gifsicle-bin/workflows/test/badge.svg?branch=main)

> gifsicle manipulates GIF image files in many different ways. Depending on command line options, it can merge several GIFs into a GIF animation; explode an animation into its component frames; change individual frames in an animation; turn interlacing on and off; add transparency and much more.

You probably want [`imagemin-gifsicle`](https://github.com/imagemin/imagemin-gifsicle) instead.

## Install

```
$ npm install gifsicle
```

Compared with the official package, this package supports setting the mirror URL. You can set the download URLs of its binary files in the following two ways:

1. Set the npm config property `imagemin_cdnurl`.

```sh
npm install pngquant-bin --imagemin_cdnurl=https://npmmirror.com/mirrors
```

2. Set the environment variables.

```sh
IMAGEMIN_CDNURL=https://npmmirror.com/mirrors npm install pngquant-bin
```

## Usage

```js
import {execFile} from 'node:child_process';
import gifsicle from 'gifsicle';

execFile(gifsicle, ['-o', 'output.gif', 'input.gif'], error => {
	console.log('Image minified!');
});
```

## CLI

```
$ npm install --global gifsicle
```

```
$ gifsicle --help
```
