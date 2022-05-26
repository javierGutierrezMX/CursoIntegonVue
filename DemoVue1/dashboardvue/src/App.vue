<template>
  <div id="main-wrapper">
        <headerComponent/>
        <breadcrumbsComponent/>
        <sidebarComponent/>
  </div>
</template>

<script>
import headerComponent from './components/shared/headerComponent.vue'
import breadcrumbsComponent from './components/shared/breadcrumbsComponent.vue'
import sidebarComponent from './components/shared/sidebarComponent.vue'
export default {
  name: 'App',
  components: {
    headerComponent,
    breadcrumbsComponent,
    sidebarComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/* <!-- Bootstrap Core CSS -->
        <link href="/assets/plugins/bootstrap/css/bootstrap.min.css" type="text/css">
        ./assets/plugins/bootstrap/css/bootstrap.min.css
        <!-- Custom CSS -->
        <link href="/assets/css/style.css" type="text/css">
        <!-- You can change the theme colors from here -->
        <link href="/assets/css/colors/default-dark.css" id="theme" type="text/css"> */
@import './assets/plugins/bootstrap/css/bootstrap.min.css';
@import './assets/css/style.css';
@import './assets/css/colors/default-dark.css';
</style>
