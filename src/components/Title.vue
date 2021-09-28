<template>
  <div class="wrapper">
      <div class="title-line"></div>
      <h2>{{title}}</h2>
  </div>
</template>

<script>
export default {
    name: 'Title',
    props: ['title'],
}
</script>

<style lang="scss">

.wrapper {
    display: flex;
    align-items: center;
    
    .title-line {
        width: 100px;
        height: 5px;
        margin-right: 25px;
        background: $black;
    }

    h2 {
        font-size: 30px;
        font-weight: bold;
    }
}

</style>