<template>
  <div class="top">
          <svg xmlns="http://www.w3.org/2000/svg" width="104" height="24" viewBox="0 0 104 24" class="top-left">
            <path id="Tracé_1" data-name="Tracé 1" d="M0,0H24V24H0Z" :fill="color"/>
            <path id="Tracé_2" data-name="Tracé 2" d="M0,0H24V24H0Z" transform="translate(80)" :fill="color"/>
            <path id="Tracé_3" data-name="Tracé 3" d="M0,0H24V24H0Z" transform="translate(40)" :fill="color"/>
        </svg>

        <div class="top-right">
            <div class="text">
                <p :style="{ color: itemColor }">{{topText}}</p>
                <p :style="{ color: itemColor }">{{bottomText}}</p>
            </div>
            <div class="line" :style="{ backgroundColor: itemColor }"></div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'Header',
    props: {
        color: {
            type: String,
            default: '#111111',
        },
        topText: {
            type: String,
            required: true,
        },
        bottomText: {
            type: String,
            required: true,
        },
    }
}
</script>

<style lang="scss">

.top {
    height: 290px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 88px 100px 100px 100px;

    .top-right {
        display: flex;
        align-items: center;
        color: $white;
        text-align: right;

        .text {
            margin-right: 20px;
        }

        .line {
            width: 5px;
            height: 100px;
        }
    }
}

</style>