<template>
  <div>
    <app-header></app-header>
    <app-servers></app-servers>
    <app-status></app-status>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import Footer from './components/Footer.vue';
  import Header from './components/Header.vue';
  import Servers from './components/Servers.vue';
  import ServerStatus from './components/ServerStatus.vue';
  export default {
    components: {
      'app-footer': Footer,
      'app-header': Header,
      'app-servers': Servers,
      'app-status': ServerStatus,
    }
  }
</script>

<style>
p {
  font-family: 'Source Sans Pro', sans-serif;
}
h1 {
  font-family: 'Source Sans Pro', sans-serif;
}
h2 {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 100;
}
button {
  padding-top: 12px;
  padding-bottom: 12px;
  padding-left: 15px;
  padding-right: 15px;
  background-color: #202b3e;
  border: none;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 16px;
  color: #fff;
}
</style>
