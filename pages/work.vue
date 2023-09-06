<template>
    <div class="bg-black h-screen px-6 py-12">
        <h2 class="text-white font-exo text-5xl opacity-0" ref="title" style="transform: translateY(30px);">MY WORK</h2>
        <div class="flex space-x-4">
            <div ref="projects" v-for="project in projects" class="w-full opacity-0" style="transform: translateX(30px);">
                <a href="https://igorson01.github.io/3dgierson/">
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
             title: 'Fight Game'
            },
            {
             image:{
                url: kulkigameImg
             },
             title: 'Kulki Game'
            },
            {
             image:{
                url: kinggameImg
             },
             title: 'King Game'
            },
            {
             image:{
                url: spaceinvadergameImg
             },
             title: 'Space Invader Game'
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