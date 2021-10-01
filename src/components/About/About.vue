<template>
  <Header color="#111111" topText="Web" bottomText="Development" />
  <Title title="About me"/>
  <Whoiam />
  <DashedLine />
  <Header color="#111111" topText="Web" bottomText="Development" />
  <Skills />

</template>

<script>
import Header from '../Header.vue';
import Title from '../Title.vue';
import Whoiam from './Whoiam.vue';
import DashedLine from './DashedLine.vue';
import Skills from './Skills.vue';

export default {
    name: 'About',
    components: {
        Header,
        Title,
        Whoiam,
        DashedLine,
        Skills,
    },
}
</script>

<style>

</style>