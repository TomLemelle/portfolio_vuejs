<template>
    <section class="skills">
        <h3>My skills</h3>
        <h4>Front<span> - END</span></h4>
        <div class="cards">
            <SkillCard :style="reactbg" name="React" desc="Javascript framework for creating dynamic web applications, i love it :)" />
            <SkillCard :style="vuebg" name="Vue" desc="Javascript framework for creating dynamic web applications, i love it :)" />
            <SkillCard :style="angularbg" name="Angular" desc="Javascript framework for creating dynamic web applications, not my favorite :(" />
        </div>
        <h4>Back<span> - END</span></h4>
        <div class="cards">
            <SkillCard :style="nodejsbg" name="Node" desc="Javascript back-end language that i use with expressjs for creating api or back-end server, i love it :)" />
            <SkillCard :style="symfonybg" name="Symfony" desc="PHP back-end & front-end framework that i use sometimes for creating api or back-end server, it's pretty cool :|" />
            <SkillCard :style="csharpbg" name="Csharp" desc="Csharp back-end mainly language, i'm currently learning it at school with it's framework ASP.NET, not my favorite :(" />
        </div>
    </section>
</template>

<script>
import SkillCard from './SkillCard.vue';
import react from '../../assets/react.png';
import vue from '../../assets/vue.png';
import angular from '../../assets/angular.png';
import nodejs from '../../assets/nodejs.png';
import symfony from '../../assets/symfony.png';
import csharp from '../../assets/csharp.png';

export default {
    name: 'Skills',
    components: {
        SkillCard,
    },
    data: () => {
        return {
            reactbg: { backgroundImage: `url(${react})` },
            vuebg: { backgroundImage: `url(${vue})` },
            angularbg: { backgroundImage: `url(${angular})` },
            nodejsbg: { backgroundImage: `url(${nodejs})` },
            symfonybg: { backgroundImage: `url(${symfony})` },
            csharpbg: { backgroundImage: `url(${csharp})` },
            name: {
                front: {
                    react: 'React',
                    vuejs: 'Vue',
                    angular: 'Angular'
                },
                back: {
                    node: 'Node',
                    symfony: 'Symfony',
                    csharp: 'Csharp',
                }
            }
        }
    }
}
</script>

<style lang="scss">
.skills {
    h4 {
        font-size: 28px;
        font-weight: bold;
        text-align: center;
        color: $green;
        &:first-of-type {
            margin-bottom: 10px;
        }
        &:last-of-type {
            margin: 10px 0;
        }

        span { color: $black; }
    }
    h3 {
        margin-left: 4%;
        text-transform: uppercase;
        font-family: 'Didot';
        font-size: 50px;
        font-weight: 400;
        margin-bottom: 75px;
    }

    .cards {
        max-width: 91.5%;
        margin: 0 auto;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 4vw;

        @media (max-width: 1114px) {
            grid-template-columns: repeat(2, 1fr);
        }
        @media (max-width: 900px) {
            grid-template-columns: 1fr;
        }
    }

}

            
</style>