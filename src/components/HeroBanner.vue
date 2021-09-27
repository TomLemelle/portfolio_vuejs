<template>
  <section class="heroBanner">
      <Header />
  </section>
</template>

<script>
import Header from './Header.vue';

export default {
    name: 'HeroBanner',
    components: {
        Header,
    }
}
</script>

<style lang="scss">

.heroBanner {
    background: $black;
    width: 100%;
    height: 100vh;
}

</style>