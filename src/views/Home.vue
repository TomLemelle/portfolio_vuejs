<template>
  <HeroBanner />
  <About />
</template>

<script>
// @ is an alias to /src
import HeroBanner from '@/components/HeroBanner/HeroBanner';
import About from '@/components/About/About';

export default {
  name: 'Home',
  components: {
    HeroBanner,
    About,
  }
}
</script>
