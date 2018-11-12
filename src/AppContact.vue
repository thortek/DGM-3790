<template>
    <div id="AppContact">
        <app-hero-contact></app-hero-contact>
        <app-form-contact></app-form-contact>
    </div>
</template>

<script>
import AppHeroContact from './components/Contact/AppHeroContact'
import AppFormContact from './components/Contact/AppFormContact'
  export default {
      name: 'AppContact',
      components: {AppHeroContact,AppFormContact},
    data: () => ({
      gradient: 'to top right, rgba(49,81,181, .3), rgba(25,32,72, .7)'
    })
  }
</script>


