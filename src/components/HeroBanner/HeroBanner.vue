<template>
  <section class="heroBanner">
      <Header color="#fff" topText="Web" bottomText="Development"/>
      <div class="center">
          <h1>Tom Lemelle</h1>
          <div class="drag"></div>
      </div>
      <Footer />
  </section>
</template>

<script>
import Header from '../Header.vue';
import Footer from '../Footer.vue';

export default {
    name: 'HeroBanner',
    components: {
        Header,
        Footer,
    }
}
</script>

<style lang="scss">

*{
    transition: all 250ms ease-out;
}
.heroBanner {
    background: $black;
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;

    .center {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        h1 {
            font-size: 130px;
            font-weight: bold;
            text-align: center;
            white-space: nowrap;
            color: $white;

            @media (max-width: 1400px) {font-size: 80px;}
            @media (max-width: 900px) {font-size: 60px;}
            @media (max-width: 660px) {font-size: 40px;}
            @media (max-width: 460px) {font-size: 30px;}
        }
    }

    .drag {
        margin-top: 50px;
        width: 54px;
        height: 140px;
        background: $white;
        border-radius: 27px;
    }
}

</style>