<template>
  <Header />
  <Title title="About me"/>
  <Whoiam />
  <DashedLine />
</template>

<script>
import Header from '../Header.vue';
import Title from '../Title.vue';
import Whoiam from './Whoiam.vue';
import DashedLine from './DashedLine.vue';
export default {
    name: 'About',
    components: {
        Header,
        Title,
        Whoiam,
        DashedLine,
    }
}
</script>

<style>

</style>