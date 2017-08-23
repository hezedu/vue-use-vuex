# vue-use-vuex
Fixed: must call Vue.use(Vuex) before creating a store instance.
## Install
`npm install vue-use-vuex`
## Example
```js
//Entry
import Vue from 'vue';
import 'vue-use-vuex';

import App from './App.vue'; //Have import some store.

new Vue({
  el: '#app',
  render: h => h(App)
})
// ... no problem
```
