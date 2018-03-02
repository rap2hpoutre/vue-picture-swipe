# Vue Picture Swipe Gallery

This component is a simple wrapper for the awesome [Photoswipe](http://photoswipe.com/).
It's a [Vue](https://vuejs.org/) plugin that displays a gallery of image with swipe function (and more). 
Includes lazy (smart) loading (mobile friendly) and thumbnails.


## Demo

<img src="https://media.giphy.com/media/F0scu9nmMJQIoJLXdF/giphy.gif">

## Install

```bash
npm install --save vue-picture-swipe
```

## Usage

You can use it as you want. Here are some examples if you want to use it inline, or in a `.vue` file component or even with Laravel. 

### Inline usage

You can using it inline:

```html
<vue-picture-swipe :items="[
    {src: 'http://example.org/xl.jpg',thumbnail: 'http://example.org/sm1.jpg',w: 600,h: 400},
    {src: 'http://example.org/xxl.jpg',thumbnail: 'http://example.org/sm2.jpg',w: 1200,h: 900}
  ]"></vue-picture-swipe>
```

Just remember to register the component:

```javascript
import VuePictureSwipe from 'vue-picture-swipe';
Vue.component('vue-picture-swipe', VuePictureSwipe);

new Vue({
  el: '#app'
})
```

### Usage in another component

Create a component `Example.vue`. Then paste this:

```vue
<template>
  <vue-picture-swipe :items="items"></vue-picture-swipe>
</template>
<script>
  import VuePictureSwipe from 'vue-picture-swipe';
  export default {
    data() {
      return {
        items: [{
          src: 'http://via.placeholder.com/600x400',
          thumbnail: 'http://via.placeholder.com/64x64',
          w: 600,
          h: 400
        },
        {
          src: 'http://via.placeholder.com/1200x900',
          thumbnail: 'http://via.placeholder.com/64x64',
          w: 1200,
          h: 900
        }
      ]};
    }
  }
</script>
```

### Usage with Laravel

Edit `resources/assets/js/app.js` and add this just before the `new Vue` lines.

```javascript
import VuePictureSwipe from 'vue-picture-swipe';
Vue.component('vue-picture-swipe', VuePictureSwipe);
```

Then run your watcher:

```sh
npm run watch
```

## Why?

I did not found any vue componant that uses thumbnail (smaller version of images) and is mobile-friendly (swipe)

 - [This one](https://github.com/LS1231/vue-preview) is documented (and issued) in chinese only and has no thumbnails.
 - [This one](https://github.com/zhaohaodang/vue-see) is documented (and issued) in chinese too and has no thumbnails either.
 - [This one](https://github.com/ymyang/vue-photoswipe) has no documentation.
 - [This one](https://github.com/SabatinoMasala/vue-simple-photoswipe) is a kind of fork of the previous one
 - ...
 
 So I created mine.
 
 <img src="https://imgs.xkcd.com/comics/standards.png">
 
 Source: https://xkcd.com/927/
