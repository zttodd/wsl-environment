# webp

## Use with build tools

To encode to `webp` using build tools, install the following node packages:

`npm install --save-dev imagemin imagemin-webp`

`imagemin` allows you to minify images, and `imagemin-webp` allows `imagemin` to minify to `webp`

Next, set up a build task. Here's an example using gulp, from [web.dev](https://web.dev/serve-images-webp/):

```
/*
 * https://web.dev/serve-images-webp/
 */

const imagemin = require('imagemin');
const imageminWebp = require('imagemin-webp');

imagemin(['images/*'], {
  destination: 'compressed_images',
  plugins: [imageminWebp({quality: 50})]
}).then(() => {
  console.log('Done!');
});
```

## Use with the command line

To encode images to `webp` using the command line, the following executables should be installed:

- `libwebp` library: used to add WebP encoding or decoding to your programs

- `cwebp`: WebP encoder tool

- `dwebp`: WebP decoder tool

- `vwebp`: WebP file viewer

- `webpmux`: WebP muxing tool

- `gif2webp`: Tool for converting GIF images to WebP

_Check out [these docs](https://developers.google.com/speed/webp/docs/precompiled) for more information about these tools._

### Installation

To install these tools, use Homebrew for Linux:

`brew install webp`
