# vue-drag
 The only required dependencies are:
* [Vue.js](http://vuejs.org/) (required ^v2.x.x, test with v2.0.3).

## Installation

### NPM
```bash
$ npm install git://github.com/shaoxiong789/vue-drag.git --save
```
```js
<template>
  <div>
    <dragboot :list="lists">
      <dragbox v-for="(item,$index) in lists" :item="item" indicate="name">
        <div slot="dragperch">
          预留空位
        </div>
        <drag slot="drag" :item="item">
          <div :style="{background:item.color}">
            拖拽目标{{item.name}}
          </div>
        </drag>
      </dragbox>
    </dragboot>
  </div>
</template>
<script>
import {dragboot,drag,dragbox} from 'vue-drag'
export default {
  components:{dragboot,drag,dragbox},
  data() {
      return {
        lists:[
          {name:'1',color:'red'},
          {name:'2',color:'orange'},
          {name:'3',color:'yellow'},
          {name:'4',color:'green'},
          {name:'5',color:'indigo'},
          {name:'6',color:'blue'},
          {name:'7',color:'purple'}
        ]
      }
  }
}
</script>
```
