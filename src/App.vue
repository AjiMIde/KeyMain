<template>
  <div id="app">
    <div id="nav" v-if="false">
      <!--<router-link to="/">Home</router-link> |-->
      <!--<router-link to="/about">About</router-link>-->
    </div>
    <bee-loading></bee-loading>
    <bee-toast></bee-toast>
    <router-view/>
  </div>
</template>

<script>
import BeeLoading from 'bee-mui/src/components/dialog/bee-loading'
import BeeToast from 'bee-mui/src/components/dialog/bee-toast'

export default {
  components: {
    BeeLoading, BeeToast
  },
  mounted () {
    window.app = this
  }
}
</script>
<style lang="scss">
  @import "~bee-mui/src/styles/bee.reset";
  html {
    /*background-image: url('assets/photo-1489573280374-2e193c63726c.jpg');*/
    /*background-attachment: fixed;*/
    /*background-blend-mode: color-burn;*/
    /*background-color: #828282 !important;*/
  }
  html, body {
    height: 100%;
  }

  #app {
    /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
    /*-webkit-font-smoothing: antialiased;*/
    /*-moz-osx-font-smoothing: grayscale;*/
    /*text-align: center;*/
    color: #2c3e50;
    /*width: 1280px;*/
    /*margin: 0 auto;*/
    height: 100%;
  }

  #nav {
    padding: 30px;
    a {
      font-weight: bold;
      color: #2c3e50;
      &.router-link-exact-active {
        color: #42b983;
        /*color: #fff;*/
      }
    }
  }
</style>
