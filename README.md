# Vue Picture Swipe Gallery

A vue plugin that displays a gallery of image with swipe function. 
Includes lazy smart loading (mobile friendly) and thumbnails.
Its backed by the awesome Photoswipe.

## Demo



## Install

```
npm install --save vue-picture-swipe
```

## Usage

You can use it as you want. Here are some examples if you want to use it inline, or in a `.vue` file component or even with Laravel. 

### Inline usage

You can using it inline:

```
<vue-picture-swipe :items="[
    {src: 'http://via.placeholder.com/600x400',thumbnail: 'http://via.placeholder.com/64x64',w: 600,h: 400},
    {src: 'http://via.placeholder.com/1200x900',thumbnail: 'http://via.placeholder.com/64x64',w: 1200,h: 900}
  ]"></vue-picture-swipe>
```

Just remember to register the component:

```
import VuePictureSwipe from 'vue-picture-swipe';
Vue.component('vue-picture-swipe', VuePictureSwipe);

new Vue({
  el: '#app'
})
```

### Usage in another component

Create a component `Example.vue`. Then paste this:

```
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

```
import VuePictureSwipe from 'vue-picture-swipe';
Vue.component('vue-picture-swipe', VuePictureSwipe);
```

Then run your watcher:

```
npm run watch
```

## Why?

I did not found any component that uses thumbnail and is mobile-friendly (swipe)

 - This one is in chinese only and has no thumbnails: https://github.com/LS1231/vue-preview
 - 