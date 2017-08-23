# wtf-vuex
Fixed: must call Vue.use(Vuex) before creating a store instance.
## Useage
```js
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

var tmp = new Vuex.Store()
tmp = null
export { Vue, Vuex }
```
