
<h3 align="center">v-page</h3>

<br><br>

<p align="center">
A simple pagination bar, including length Menu, i18n support, based on Vue2.x
</p>

<p align="center"><img src="https://terryz.github.io/image/v-page/v-page.png" alt="v-page" height="54px"></p>

<p align="center">
  <a href="https://www.npmjs.com/package/v-page"><img src="https://img.shields.io/npm/v/v-page.svg"></a>
  <a href="https://mit-license.org/"><img src="https://img.shields.io/badge/license-MIT-brightgreen.svg"></a>
  <a href="https://www.npmjs.com/package/v-page"><img src="https://img.shields.io/npm/dy/v-page.svg"></a>
</p>
<br><br><br><br><br>


## Demo、Document、Changelog
Explorer on

- [English official site](https://terryz.github.io/vue)
- [中文官网](https://terryz.gitee.io/vue)

the jQuery version: [bPage](https://github.com/TerryZ/bPage)

<br><br>

## Install

``` bash
# install dependencies
npm install v-page --save
```

Include plugin in your `main.js` file.

```js
import Vue from 'vue'
import vPage from 'v-page';
...

Vue.use(vPage);
```

## Deploy on your component

template code

```html
<template>
  <!-- v-bind 'setting' data to config page bar -->
  <!-- bind event 'page-change' to receive page info change -->
  <v-page :setting="pageSet" @page-change="pageChange"></v-page>
</template>
```

script code

```js
export default {
  name: 'myComponent',
  data(){
    return {
      pageSet: {
        totalRow: 0,//required option
        language: 'en',//default: 'cn'
        pageSizeMenu: [20,100]//default: [10, 20, 50, 100]
      }
    }
  },
  methods:{
    //receive page info change callback
    pageChange(pInfo){
      console.log(pInfo);//{pageNumber: 1, pageSize: 10}
    }
  }
};
```
