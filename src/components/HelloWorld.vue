<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank">
          Core Docs
        </a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank">
          Forum
        </a>
      </li>
      <li>
        <a href="https://chat.vuejs.org" target="_blank">
          Community Chat
        </a>
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank">
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a href="http://vuejs-templates.github.io/webpack/" target="_blank">
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a href="http://router.vuejs.org/" target="_blank">
          vue-router
        </a>
      </li>
      <li>
        <a href="http://vuex.vuejs.org/" target="_blank">
          vuex
        </a>
      </li>
      <li>
        <a href="http://vue-loader.vuejs.org/" target="_blank">
          vue-loader
        </a>
      </li>
      <li>
        <a href="https://github.com/vuejs/awesome-vue" target="_blank">
          awesome-vue
        </a>
      </li>
    </ul>
    <!-- Standard button -->
    <button type="button" class="btn btn-default" @click="change(1)">（默认样式）Default</button>

    <!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
    <button type="button" class="btn btn-primary" @click="change(2)">（新样式）Primary</button>

    <!-- Indicates a successful or positive action -->
    <button type="button" class="btn btn-success">（成功）Success</button>

    <!-- Contextual button for informational alert messages -->
    <button type="button" class="btn btn-info">（一般信息）Info</button>

    <!-- Indicates caution should be taken with this action -->
    <button type="button" class="btn btn-warning">（警告）Warning</button>

    <!-- Indicates a dangerous or potentially negative action -->
    <button type="button" class="btn btn-danger">（危险）Danger</button>

    <!-- Deemphasize a button by making it look like a link while maintaining button behavior -->
    <button type="button" class="btn btn-link">（链接）Link</button>
    <div class="alert alert-warning alert-dismissible" role="alert">
      <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span
          aria-hidden="true">&times;</span></button>
      <strong>Warning!</strong> Better check yourself, you're not looking too good.
    </div>
    <div class="btn-group" role="group" aria-label="...">
      <button type="button" class="btn btn-default">1</button>
      <button type="button" class="btn btn-default">2</button>

      <div class="btn-group" role="group">
        <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true"
          aria-expanded="false">
          Dropdown
          <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="#">Dropdown link</a></li>
          <li><a href="#">Dropdown link</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    methods:{
      change(type) {
        axios.get('http://127.0.0.1:7001/index')
          .then(function (res) {
            console.log(res);
          })
          .catch(function (error) {
            console.log(error);
          });
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  .hello{
    h2{color: #00FFFF;
    display: flex;
    justify-content: center;
    align-items: center;}
  }

</style>
