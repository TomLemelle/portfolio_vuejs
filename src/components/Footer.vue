<template>
  <div class="bottom">
      <div class="bottom-right">
            <div class="line"></div>
            <div class="text">
                <p>Creative</p>
                <p>Portfolio</p>
            </div>
        </div>

        <div class="bottom-left">
            <p>2021</p>
        </div>
      </div>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style lang="scss">

.bottom {
    height: 290px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 88px 100px 100px 100px;

    .bottom-left {
        p {
            font-weight: bold;
            font-size: 25px;
            color: $white;
        }
    }

    .bottom-right {
        display: flex;
        align-items: center;
        color: $white;
        text-align: left;

        .text {
            margin-left: 20px;
        }

        .line {
            width: 5px;
            height: 100px;
            background: $white;
        }
    }
}

</style>