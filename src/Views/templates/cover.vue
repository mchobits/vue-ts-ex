<template>

 <div class="site-wrapper">

      <div class="site-wrapper-inner">

        <div class="cover-container">

          <div class="masthead clearfix">
            <div class="inner">
              <h3 class="masthead-brand">logo</h3>
              <nav class="nav nav-masthead">
                <a class="nav-link active" href="#">Home</a>
                <a class="nav-link" href="#">Features</a>
                <a class="nav-link" href="#">Contact</a>
              </nav>
            </div>
          </div>

          <div class="inner cover">
            <h1 class="cover-heading">Cover me cover you.</h1>
            <p class="lead">Cover is a one-page template for building simple and beautiful home pages. Download, edit the text, and add your own fullscreen background photo to make it your own.</p>
            <p class="lead">
              <a href="#" class="btn btn-lg btn-secondary">Learn more</a>
            </p>
          </div>

          <div class="mastfoot">
            <div class="inner">
              <p>Cover template for <a href="https://getbootstrap.com">Bootstrap</a>, by <a href="https://twitter.com/mdo">@mdo</a>.</p>
            </div>
          </div>

        </div>

      </div>

    </div>

</template>
<script lang="ts">
//CSS It's recommended to combine it with the css-loader: require("style!css!./file.css").
//var navbar = require('./src/components/navbar.vue').default
//require('style-loader!css-loader!./Todolist.css').toString(‌​)
//var cstyle = require("css-loader!./src/assets/AT/style.css").toString(‌​)
//import './src/assets/AT/style.css'
//var ExtractTextPlugin = require("extract-text-webpack-plugin");
import  navbar from '../../components/navbar.vue'
import  store  from '../../System/store'
import {Component, create, getHelper,Vue, Store,Lifecycle }  from './ext'


//require("css!./src/assets/AT/style.css");
//require("style!raw!./src/assets/AT/style.css");
//require("style!raw!./src/assets/AT/style.css")
//import Vue from "./node_modules/vue/dist/vue.common.js";

//import 'tether';
//import "jquery";

//import "bootstrap-select/dist/js/bootstrap-select.js";
//var bo = require('bootstrap-vue').default;
//Vue.use(bo);

@Component({  components:{ navbar  }  // multiselect:multiselect,vselect:vselect bo.alert, dropdown:bo.dropdown

 }) //,separatets, about , Bootstrap
export default class App extends Vue {
  name = 'App'
  loc = 'at'

  //example of manipulating central store values
  @Lifecycle mounted() {
       //here you show the alert
       console.log('app mounted')       
    }
}
 </script>
<style lang="less" >
  @import url("./../node_modules/bootstrap/dist/css/bootstrap.min.css");
 /*  @import "./node_modules/bootstrap-select/dist/css/bootstrap-select.css";*/
  /*@import "//maxcdn.bootstrapcdn.com/bootswatch/3.3.6/sandstone/bootstrap.min.css"*/
/*
 * Globals
 */

/* Links */
a,
a:focus,
a:hover {
  color: #fff;
}

/* Custom default button */
.btn-secondary,
.btn-secondary:hover,
.btn-secondary:focus {
  color: #333;
  text-shadow: none; /* Prevent inheritance from `body` */
  background-color: #fff;
  border: .05rem solid #fff;
}


/*
 * Base structure
 */

html,
body {
  height: 100%;
  background-color: #333;
}
body {
  color: #fff;
  text-align: center;
  text-shadow: 0 .05rem .1rem rgba(0,0,0,.5);
}

/* Extra markup and styles for table-esque vertical and horizontal centering */
.site-wrapper {
  display: table;
  width: 100%;
  height: 100%; /* For at least Firefox */
  min-height: 100%;
  -webkit-box-shadow: inset 0 0 5rem rgba(0,0,0,.5);
          box-shadow: inset 0 0 5rem rgba(0,0,0,.5);
}
.site-wrapper-inner {
  display: table-cell;
  vertical-align: top;
}
.cover-container {
  margin-right: auto;
  margin-left: auto;
}

/* Padding for spacing */
.inner {
  padding: 2rem;
}


/*
 * Header
 */

.masthead {
  margin-bottom: 2rem;
}

.masthead-brand {
  margin-bottom: 0;
}

.nav-masthead .nav-link {
  padding: .25rem 0;
  font-weight: bold;
  color: rgba(255,255,255,.5);
  background-color: transparent;
  border-bottom: .25rem solid transparent;
}

.nav-masthead .nav-link:hover,
.nav-masthead .nav-link:focus {
  border-bottom-color: rgba(255,255,255,.25);
}

.nav-masthead .nav-link + .nav-link {
  margin-left: 1rem;
}

.nav-masthead .active {
  color: #fff;
  border-bottom-color: #fff;
}

@media (min-width: 48em) {
  .masthead-brand {
    float: left;
  }
  .nav-masthead {
    float: right;
  }
}


/*
 * Cover
 */

.cover {
  padding: 0 1.5rem;
}
.cover .btn-lg {
  padding: .75rem 1.25rem;
  font-weight: bold;
}


/*
 * Footer
 */

.mastfoot {
  color: rgba(255,255,255,.5);
}


/*
 * Affix and center
 */

@media (min-width: 40em) {
  /* Pull out the header and footer */
  .masthead {
    position: fixed;
    top: 0;
  }
  .mastfoot {
    position: fixed;
    bottom: 0;
  }
  /* Start the vertical centering */
  .site-wrapper-inner {
    vertical-align: middle;
  }
  /* Handle the widths */
  .masthead,
  .mastfoot,
  .cover-container {
    width: 100%; /* Must be percentage or pixels for horizontal alignment */
  }
}

@media (min-width: 62em) {
  .masthead,
  .mastfoot,
  .cover-container {
    width: 42rem;
  }
}

</style>