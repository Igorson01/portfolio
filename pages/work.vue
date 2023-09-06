<template>
    <div class="bg-black h-screen px-6 py-12">
        <h2 class="text-white font-exo text-5xl opacity-0" ref="title" style="transform: translateY(30px);">MY WORK</h2>
        <div class="flex space-x-4">
            <div ref="projects" v-for="project in projects" class="w-full opacity-0" style="transform: translateX(30px);">
                <a :href="project.link">
        <img :src="project.image.url" alt="FightGame" style="height: 70vh;" class="object-cover">
        <p class="text-white font-space-mono text-sm">{{ project.title }}</p>
                </a>
           </div>
        </div>
    </div>
</template>
<script>
import gsap from 'gsap'
import fightgameImg from '~/assets/fightgame.png'
import kulkigameImg from '~/assets/kulkigame.png'
import kinggameImg from '~/assets/kinggame.png'
import spaceinvadergameImg from '~/assets/spaceinvadergame.png'
export default{
    data() {
        return {
            projects:[
            {
             image:{
                url: fightgameImg
             },
             title: 'Fight Game',
             link:'https://64f864bbdd155770de5a8338--dapper-sundae-da5b6e.netlify.app/'
            },
            {
             image:{
                url: kulkigameImg
             },
             title: 'Kulki Game',
             link:'https://64f867454c94e174a2e0e56f--extraordinary-cheesecake-36b642.netlify.app/'
            },
            {
             image:{
                url: kinggameImg
             },
             title: 'King Game',
             link: 'https://64f8679dbe2880747c0bdd7c--fluffy-bienenstitch-57d48a.netlify.app/'
            },
            {
             image:{
                url: spaceinvadergameImg
             },
             title: 'Space Invader Game',
             link:'https://64f867e8dd155773f35a81e5--subtle-paprenjak-b331f0.netlify.app/'
            },
            {
             image:{
                url: fightgameImg
             },
             title: 'Fight Game'
            },
            {
             image:{
                url: kulkigameImg
             },
             title: 'Kulki Game'
            }
            ]
        }
    },
    mounted() {
    gsap.to(this.$refs.title, {
        opacity:1,
        duration:1.5,
        y:0,
        ease: 'expo'
    })

    gsap.to(this.$refs.projects, {
        opacity:1,
        duration:1.5,
        stagger:0.1,
        x:0,
        ease: 'expo',
        delay:0.3
    })
    }
}
</script>
<style>.font-exo {
    font-family: 'Exo 2', sans-serif;
  }
  .font-space-mono{
    font-family: 'Space Mono', monospace;
  }
</style>