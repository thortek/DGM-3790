<template>

        <app-header></app-header>
        <hr>
        <div class="boxes">
        <app-servers></app-servers>
        </div>
        <hr>
        <app-footer></app-footer>
        
</template>

<script>
    import Header from './components/Header.vue';
    import Footer from './components/Footer.vue';
    import Servers from './components/Servers.vue';
    import ServerDetails from './components/ServerDetails.vue';

    export default {
        components: {
            'app-header': Header,
            'app-servers': Servers,
            'app-server-details': ServerDetails,
            'app-footer': Footer
        }
    }
</script>

<style>
.boxes {
  border: solid 1px #f8f8f8;
  padding: 30px;
  background-color: #f2f2f2;
}
</style>
