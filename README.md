# vue-use-vuex
Fixed: must call Vue.use(Vuex) before creating a store instance.

If you normally use vuex, just like this:
```js
// Entry
import Vue from 'vue';
import Vuex from 'vuex';
Vue.use(Vuex);
import 'some-store.js';
```
You Will get an Error:<br/>
![image](https://github.com/hezedu/SomethingBoring/blob/master/static/vue-use-vuex.png?raw=true)<br/>
WTF! 

let's use **vue-use-vuex** to fixed it.
## Install
`npm install vue-use-vuex`

## Example
```js
// Entry
import Vue from 'vue';
import 'vue-use-vuex'; // Just should import once
import 'some-store.js';

// no problem!
```
## webpack-1
If you used webpack 1.x, you should used loader's include:
```js
var vueUseVuexPath = require.resolve('vue-use-vuex');

// ...
    {
      test: /\.js$/,
      include: [path.join(__dirname, "src"), vueUseVuexPath],
      loader: 'babel-loader'
    }
```
