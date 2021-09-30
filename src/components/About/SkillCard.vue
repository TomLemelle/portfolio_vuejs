<template>
    <div class="card">
        <div class="skill-name">{{name}}</div>
        <div class="skill-description">{{desc}}</div>
    </div>
</template>

<script>
export default {
    name: 'SkillCard',
    props: {
        name: {
            type: String,
            required: true,
        },
        desc: {
            type: String,
        },
    },
    components: {
    },
}
</script>

<style lang="scss">

.card {
    height: 150px;
    padding-top: 16px;
    padding-bottom: 16px;
    padding-left: 12px;
    border-right: 10px solid $green;
    position: relative;
    overflow: hidden;
    color: #fff;
    background-position: 95% 50%;
    background-size: 70px;
    background-repeat: no-repeat;
    background-color: $black;
    transition: color .8s cubic-bezier(.16,1,.3,1);

    .skill-name {
        font-size: 1.25vw;
        position: relative;
        z-index: 1;
        line-height: 1em;
    }

    .skill-description {
        font-size: .7vw;
        font-weight: normal;
        margin-top: 12px;
        max-width: 70%;
        position: relative;
        z-index: 1;
        @media (max-width: 1114px) {
            font-size: .9vw;
        }
        @media (max-width: 900px) {
            font-size: 10px;
        }
    }
}
</style>