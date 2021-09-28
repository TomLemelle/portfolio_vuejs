<template>
  <Header />
  <Title title="About me"/>
  <Whoiam />
</template>

<script>
import Header from '../Header.vue';
import Title from '../Title.vue';
import Whoiam from './Whoiam.vue';

export default {
    name: 'About',
    components: {
        Header,
        Title,
        Whoiam,
    }
}
</script>

<style>

</style>