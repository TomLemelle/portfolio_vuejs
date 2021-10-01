<template>
    <ul class="whoiam">
        <li class="text">
            <h3>Who i am</h3>
            <p>Im a french front & back developer </p>
            <p>Ut placerat nisi eu dolor mollis, et ultrices massa venenatis.</p>
            <p>Vivamus malesuada euismod leo ac condimentum.</p>
            <p>Integer sit amet lacus tincidunt, feugiat ligula vitae, viverra est.</p>
        </li>
        <li class="image">
            <div class="shadow"></div>
            <img src="@/assets/moi.jpg" alt="a picture of me (tom lemelle)">
            <div class="effect-mobile">
                <img src="@/assets/left-me.png" class="mobile" alt="a picture of me (tom lemelle)">
                <img src="@/assets/mid-me.png" class="mobile-mid" alt="a picture of me (tom lemelle)">
                <img src="@/assets/right-me.png" class="mobile" alt="a picture of me (tom lemelle)">
            </div>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'Whoiam',
}
</script>

<style lang="scss">

.whoiam {
    position: relative;
    margin: 110px auto 60px; 
    list-style: none;
    max-width: 1065px;
    height: auto;
    @media (max-width: 1130px) {
        max-width: 90%;
        position: static;
    }

    .text {
        position: absolute;
        z-index: 1000;
        top: 0;
        left: 0;
        @media (max-width: 1130px) {
            position: static;
            text-align: center;
        }

        h3 {
            display: inline-flex;
            border: 1px solid #111111;
            padding: 15px;
            margin-bottom: 45px;
            text-transform: uppercase;
            font-family: 'Didot';
            font-size: 50px;
            font-weight: 400;
        }

        p {
            font-family: 'Roboto Mono';
            font-weight: normal;
            font-size: 20px;
            color: $green;
            mix-blend-mode: difference;
        }
    }

    .image {
        position: relative;
        z-index: 1;
        top: -82px;
        right: -50%;
        width: 445px;
        height: 405px;
        &::before, &::after{
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: $black;
        }

        &::before { top: -15px; right: -15px; z-index: -1;}
        &::after { top: 0; right: -15px; z-index: -2;}

        @media (max-width: 1130px) { 
            width: 100%;
            height: auto;
            position: unset;

            & > img { display: none;}
        }

        .effect-mobile {
            display: none;
        }

        @media (max-width: 1130px) {
            .effect-mobile {
                display: grid;
                grid-template-columns: 1fr 1fr 1fr;
                grid-column-gap: 50px;
                margin-top: 40px;

                &:hover {
                    grid-column-gap: 0;
                }
            }
        }

        img {
            width: 100%;
        }
    }
}

</style>