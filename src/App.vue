<template lang='pug'>
  .app
    h1.texto Escoge personaje 
    .img(v-if="isMiguel" @click="chooseN") 
        img(src='/static/Miguel.png' whidth="200px" height="200px")
    .img(v-if="isNicolas" @click="chooseM")
        img(src='/static/Nicolas.png' whidth="200px" height="200px")
    .texto1(v-if="isTexto1") MIGUEL
      .left 
        .line A 20 year-old young man who has been a slave his entire life and that works for mister Nicolas at “El paraiso” the biggest ranch in town.

    .texto1_1(v-if="isTexto1_1")
      h3.letra.espacio Welcome to the first level, there are a lot of things to know, so if you want to find out read the story, my story. 
      .left.espacio
        .line My “mamma” and my “pappa” arrived to the city of slaves in 1586, they were brought here in big white-red boats from their villages in South Africa; they told me that they were taken to some rooms under a ship, where there were hundreds of people that they knew. As soon as they got to these rooms they had to take off their clothes and were given some pieces of clothing to cover their private parts, they spent almost 6 months in there, in which some people died due to lack of food, water and some diseases. After spending that time there, they arrived to a big place called Cartagena, where they were taken  to meet the rich white people; then they examined them to see if they had any flaw as if they were things and just started to separate the families, back then my parents did not know what was happening because they didn’t speak their language, but what they understood later was that, the day that they arrived to the town they were sold like animals.
      .left.espacio 
        .line My mamma Lorenza told me that she and my pappa Andres were lucky because they were bought by the same man Mr. Nicolas, the richest man in town. They have worked for him for the last 20 years, so after some time they decided to have me, my name is Miguel and I was born as a slave. I grew up in the biggest ranch in town “El paraíso”. I have to say that our master is kind to us, he never punishes us when is not necessary and he gives us tasty food, he even allows us to go to the cabildos, they are like big parties where we gather to have a good time and sometimes to speak about the cause. But, lately I have realised that sometimes they abuse us when the only thing we do is serve them. Before, when I was a kid I thought that this was the best life I could have, now that I have grown up I think that we deserve better.

    h3.preguntas(v-if="isCuestionarioMiguel") In order to unlock the following level, you will have to restate the sentences below, using no more than three words per answer. You must have at least 4 out of 7 correct answers. 
    .texto1_2(v-if="isTexto1_2") Question
      .left
        .line I. Some of the Africans that were in the ship did not arrive in Cartagena because they did not 
        input.res(v-model="resMig1" :class="{red: !isResMi1 && resMig1 != ''}" type="text" placeholder="completar")

      .left 
        .line II. When Miguel’s parents arrived to mainland they were checked in order to determine if they
        input.res(v-model="resMig2" :class="{red: !isResMi2 && resMig2 != ''}" type="text" placeholder="completar") 
        .line so white people could establish their price

      .left 
        .line III. Lorenza felt happy when Mr. Nicolas bought her because he
        input.res(v-model="resMig3"  :class="{red: !isResMi3 && resMig3 != ''}" type="text" placeholder="completar")

      .left
        .line IV. Since Miguel was born in
        input.res(v-model="resMig4" :class="{red: !isResMi4 && resMig4 != ''}"  type="text" placeholder="completar") 
        .line in 1606, he has been a
        input.res(v-model="resMig4_1" :class="{red: !isResMi4_1 && resMig4_1 != ''}" type="text" placeholder="completar")

      .left
        .line V. Miguel thinks that Mr. Nicolas is
        input.res(v-model="resMig5" :class="{red: !isResMi5 && resMig5 != ''}" type="text" placeholder="completar") 
        .line because he hardly ever punishes him.
      
      .left
        .line VI. Miguel is not happy with his life, he thinks slaves should be
        input.res(v-model="resMig6" :class="{red: !isResMi6 && resMig6 != ''}" type="text" placeholder="completar")
      
      .boton(@click="confirDat") Comprobar

    .img(v-if="isEjemplo")  
      img(src='/static/Ejemplo.png'  height="1500px")
</template>

<script>
export default {
  name: 'app',

  data () {
    return {
      isMiguel: true,
      isNicolas: true,
      isEjemplo: false,

      isTexto1: false,
      isTexto1_1: false,
      isTexto1_2: false,
      isCuestionarioMiguel: false,
      isTexto2: false,
      resMig1: '',   
      resMig2: '',  
      resMig3: '',  
      resMig4: '', 
      resMig4_1: '', 
      resMig5: '',
      resMig6: '',
      isResMi1: true,
      isResMi2: true,
      isResMi3: true,
      isResMi4: true,
      isResMi4_1: true,
      isResMi5: true,
      isResMi6: true,
      contar: 0
    }
  },

  methods:{
    chooseN(){
      this.isNicolas = false
      this.isTexto1 = true
      this.isTexto1_1 = true
      this.isTexto1_2 = true
      this.isCuestionarioMiguel = true

    },
    chooseM(){
      this.isMiguel=false
      this.isTexto2 = true
    },
    confirDat(){
      if (this.isResMi1 =  this.resMig1 == 'survive the journey' ) {
        this.contar++
      }
      if (this.isResMi2 = this.resMig2 == 'had any flaws') {
        this.contar++
      }
      if (this.isResMi3 =  this.resMig3 == 'also bought Andres') {
        this.contar++
      }
      if (this.isResMi4 =  this.resMig4 == 'Cartagena-city of slaves') {
        this.contar++
      }
      if (this.isResMi4_1 =  this.resMig4_1 == 'slave') {
        this.contar++
      }   
      if (this.isResMi5 =  this.resMig5 == 'a good master - benevolent - caring') {
        this.contar++
      }
      if (this.isResMi6 =  this.resMig6 == 'treated better') {
        this.contar++ 
      }
      if (this.contar >= 4) {
        this.isEjemplo = true
      }
    }
  }
}
</script>
<style lang='stylus'>
  .app

  .textoD
    text-align center
    font-size 30px
    margin 45px

  .img
    padding 5px 5px 5px 5px
    margin 50px 80px
    display inline-block
    vertical-align middle
    cursor pointer

  .texto1
    width 300px
    border 3px solid black 
    display inline-block
    vertical-align middle

  .texto1_1
    width 900px
    border 4px solid black 
    display block
    margin auto

  .texto1_2
    font-size 20px
    width 700px
    border 4px solid black 
    display block
    margin auto

  .res
    width 150px
    display inline
    margin 0px 5px

  .line
    display inline
    font-size 20px

  .left
    text-align left
    padding  5px 0px
  
  .letra
    font-size 20px
  
  .espacio
    padding-top 20px
  
  .preguntas
    font-size 20px

  .boton 
    color white
    background-color #1B2631
    border-radius 20px
    text-align center
    display inline-block
    padding 10px
    cursor pointer
  .boton:hover
    background-color green
  
  .red
    border 1px solid red

</style>
