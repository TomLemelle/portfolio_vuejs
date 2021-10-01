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

    @media (max-width: 600px) {
        flex-direction: column;
        justify-content: center;
    }

    .bottom-left {
        @media (max-width: 600px) { order: 1; margin-bottom: 15px;}
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

        @media (max-width: 600px) { 
            order: 2;
            position: relative;
            text-align: center;
        }

        .text {
            margin-left: 20px;
            @media (max-width: 600px) { 
                margin: 0;
            }

        }

        .line {
            width: 5px;
            height: 100px;
            background: $white;

            @media (max-width: 600px) {
                position: absolute;
                bottom: -15px;
                right: 0;
                left: 50%;
                transform: translateX(-50%);
                width: 170px;
                height: 5px;
            }
        }
    }
}

</style>