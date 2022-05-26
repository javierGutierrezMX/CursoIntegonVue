<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <hr/>
    <MatematicoDemo :num1="5" :num2="5" operacion='+'/>
    <hr/>
    <PugDemoVue/>
    <hr/>
    <CuentaCaracteres/>
    <hr/>
    <Exe7Libro/>
    <hr/>
    <CarritoDeCompras/>
    <hr/>
    <EjemplosDataVue/>
    <hr/>
    <SearchComponentVue/>
    <hr/>
    <!-- Aqui poner los k faltan -->
    <hr/>
    <MessageFeed :messages="messages" />
    <MessageEditor @send="onSend($event)" />
    
  </div>
</template>
<!-- 
  Agregar ejercicios del libro,  2.04.2.05.2.0.6,4.05,4.06 ACTIVIDAD 2 y 4 (creo k 3)
 -->
<script>
import HelloWorld from './components/HelloWorld.vue'
import MatematicoDemo from './components/MatematicoDemo.vue'
import PugDemoVue from './components/PugDemo.vue'
import CuentaCaracteres from "./components/CuentaCaracteres.vue";
import Exe7Libro from './components/Exe7Libro.vue'
import CarritoDeCompras from './components/CarritoDeCompras.vue';
import EjemplosDataVue from './components/EjemplosData.vue';
import SearchComponentVue from './components/SearchComponent.vue';
import MessageEditor from './components/MessageEditor.vue'
import MessageFeed from './components/MessageFeed.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MatematicoDemo,
    PugDemoVue,
    CuentaCaracteres,
    Exe7Libro,
    CarritoDeCompras,
    EjemplosDataVue,
    SearchComponentVue,
    MessageEditor,
    MessageFeed
  },
  methods: {
    onSend(event) {
      this.messages = [...this.messages, event]
    }
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
</style>
<!-- v-text enlaza una propiedad a un elemento html -->
<!-- v-html genera un elemento html dentro o le da props -->
<!--  -->
