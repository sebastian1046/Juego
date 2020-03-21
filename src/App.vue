<template lang='pug'>
  .app
    // Miguel
    h1.texto First, you must choose your avatar for the game, do you want to be … 
    .img(v-if="isMiguel" @click="chooseN") 
        img(src='/static/Miguel.png' whidth="200px" height="200px")
    .texto1(v-if="isTexto1") MIGUEL
      .left 
        .line A 20 year-old young man who has been a slave his entire life and that works for mister Nicolas at “El paraiso” the biggest ranch in town.

    .texto1_1(v-if="isTexto1_1")
      h3.letra.espacioPrimero Welcome to the first level, there are a lot of things to know, so if you want to find out read the story, my story. 
      .left.espacioPrimero
        .line My “mamma” and my “pappa” arrived to the city of slaves in 1586, they were brought here in big white-red boats from their villages in South Africa; they told me that they were taken to some rooms under a ship, where there were hundreds of people that they knew. As soon as they got to these rooms they had to take off their clothes and were given some pieces of clothing to cover their private parts, they spent almost 6 months in there, in which some people died due to lack of food, water and some diseases. After spending that time there, they arrived to a big place called Cartagena, where they were taken  to meet the rich white people; then they examined them to see if they had any flaw as if they were things and just started to separate the families, back then my parents did not know what was happening because they didn’t speak their language, but what they understood later was that, the day that they arrived to the town they were sold like animals.
      .left.espacioPrimero 
        .line My mamma Lorenza told me that she and my pappa Andres were lucky because they were bought by the same man Mr. Nicolas, the richest man in town. They have worked for him for the last 20 years, so after some time they decided to have me, my name is Miguel and I was born as a slave. I grew up in the biggest ranch in town “El paraíso”. I have to say that our master is kind to us, he never punishes us when is not necessary and he gives us tasty food, he even allows us to go to the cabildos, they are like big parties where we gather to have a good time and sometimes to speak about the cause. But, lately I have realised that sometimes they abuse us when the only thing we do is serve them. Before, when I was a kid I thought that this was the best life I could have, now that I have grown up I think that we deserve better.

    h3.preguntas(v-if="isCuestionarioMiguel") In order to unlock the following level, you will have to restate the sentences below, using no more than three words per answer. You must have at least 4 out of 7 correct answers. 
    .texto1_2(v-if="isTexto1_2") Question
      .left
        .line I. Some of the Africans that were in the ship did not arrive in Cartagena because they did not 
        input.res(v-model="resMig1" :class="{red: !isResMi1 && resMig1 != ''}" type="text" placeholder="complete")

      .left 
        .line II. When Miguel’s parents arrived to mainland they were checked in order to determine if they
        input.res(v-model="resMig2" :class="{red: !isResMi2 && resMig2 != ''}" type="text" placeholder="complete") 
        .line so white people could establish their price

      .left 
        .line III. Lorenza felt happy when Mr. Nicolas bought her because he
        input.res(v-model="resMig3"  :class="{red: !isResMi3 && resMig3 != ''}" type="text" placeholder="complete")

      .left
        .line IV. Since Miguel was born in
        input.res(v-model="resMig4" :class="{red: !isResMi4 && resMig4 != ''}"  type="text" placeholder="complete") 
        .line in 1606, he has been a
        input.res(v-model="resMig4_1" :class="{red: !isResMi4_1 && resMig4_1 != ''}" type="text" placeholder="complete")

      .left
        .line V. Miguel thinks that Mr. Nicolas is
        input.res(v-model="resMig5" :class="{red: !isResMi5 && resMig5 != ''}" type="text" placeholder="complete") 
        .line because he hardly ever punishes him.
      
      .left
        .line VI. Miguel is not happy with his life, he thinks slaves should be
        input.res(v-model="resMig6" :class="{red: !isResMi6 && resMig6 != ''}" type="text" placeholder="complete")
      
      .boton(@click="confirDatMig") Comprobar

    h3.espacioSegundo.letra(v-if="isEjemplo") Second:
      .left
        .line Now that you have pass the first level, everything gets a little bit more difficult. In order to pass this level and win the game you will have to pay close attention to what is next. 
    .left.letra(v-if="isEjemplo")
      .line You will read an infographic where you will find the description of black Cabildos and their importance for us. 

    .img(v-if="isEjemplo")  
      img(src='/static/ejemplo.png'  height="1500px")
    
    .espacioSegundo.left(v-if="isEjemplo") MIGUEL:
      .letra The mayor of Cartagena has given you the opportunity to present him a letter exposing the reasons why you think the Cabildos should not be eliminated, you are allowed to use an informal register and can have access to Mr. Alonso Restrepo’s help, the mayor’s assistant. You have to write a letter with no more than 10 lines, use basic structures (present simple). Here there are some expressions that you can use in order to express yourself better.

    // Nicolas
    .img(v-if="isNicolas" @click="chooseM")
        img(src='/static/Nicolas.png' whidth="200px" height="200px")
    .texto1(v-if="isTexto2") NICOLAS
      .left 
        .line A 40 year-old man who owns most of the businesses in Cartagena, he has more than 40 slaves and a wealthy life, he is the richest man in town.

    .texto1_1(v-if="isTexto2_1")
      h3.letra.espacioPrimero Welcome to the first level, my life is so wonderful and luxurious that I beg you want to know everything, so what are you waiting for? Go and read my story. 

      .left.espacioPrimero
        .line I was born in Cartagena in 1566, my parents arrived to this place from Spain, because my father was told that this land was thriving and that he would become rich, so he brought my mother here and now we are the richest family in town. When I was 15 my father died from a unknown disease, so I had to take control of the money like the man I am. Some years passed and I got into the slaves business, so I started buying black africans to serve me and my family, and to work on my plantations and ranches. I remember the first time I went to the debarkation of slaves, it was April 12th 1586, I was 20 years old and felt really nervous. When the negroes arrived they were all filthy, skinny and they stank.

      .left.espacioPrimero 
        .line I was so shocked by their appearance that I was just standing in front of them when Coronel Quintero told me to check on some of them, to see if they had flaws and if they didn’t, I could choose which ones to buy. I looked at them but I didn’t want to touch them, at the end I bought three: one man, one woman, and a teenager, their names are Andres, Lorenza and Juan, they were my first slaves, and have worked for me for the past 20 years; now I have 45 slaves. I know I am a great master, I treat them well, as long as they are good, I hardly ever wipe them and I feed them, I even allow them to go to their gatherings, they call them cabildos, I don’t know exactly what they do there, but lately I have been more concerned because after those meetings they arrived to the ranch a little bit more haughty and they don’t like to work that much, I don’t know what’s wrong with them.

    h3.preguntas(v-if="isCuestionarioNicolas") In order to unlock the following level you will have to restate the sentences below, using no more than three words per answer. You must have at least 5 out of 8 correct answers.  
    .texto1_2(v-if="isTexto2_2") Question
      .left
        .line I. When Nicolas was 15 he became 
        input.res(v-model="resNic1" :class="{red: !isResNi1 && resNic1 != ''}" type="text" placeholder="complete")
        .line of his father’s properties.
      .left 
        .line II. In order to have workforce Nicolas started to
        input.res(v-model="resNic2" :class="{red: !isResNi2 && resNic2 != ''}" type="text" placeholder="complete") 

      .left 
        .line III. When Nicolas saw the slaves for the first time he was
        input.res(v-model="resNic3"  :class="{red: !isResNi3 && resNic3 != ''}" type="text" placeholder="complete")
        .line because of their
        input.res(v-model="resNic3_1"  :class="{red: !isResNi3_1 && resNic3_1 != ''}" type="text" placeholder="complete")
      
      .left
        .line IV. Andres, Lorenza and Juan were
        input.res(v-model="resNic4" :class="{red: !isResNi4 && resNic4 != ''}"  type="text" placeholder="complete") 
        .line , so Nicolas bought them.

      .left
        .line V. Nicolas considers himself a
        input.res(v-model="resNic5" :class="{red: !isResNi5 && resNic5 != ''}" type="text" placeholder="complete") 
        .line because he treats his slaves in a good way.
      
      .left
        .line VI. Slaves have become 
        input.res(v-model="resNic6" :class="{red: !isResNi6 && resNic6 != ''}" type="text" placeholder="complete")
        .line since they attend to the cabildos, which makes Nicolas
        input.res(v-model="resNic6_1" :class="{red: !isResNi6_1 && resNic6_1 != ''}" type="text" placeholder="complete")
      .boton(@click="confirDatNic") Comprobar

    h3.espacioSegundo.letra(v-if="isEjemploNico") Second:
      .left
        .line Now that you have pass the first level, everything gets a little bit more difficult. In order to pass this level and win the game you will have to pay close attention to what is next. 
    .left.letra(v-if="isEjemploNico")
      .line You will read an infographic where you will find the description of black Cabildos and their importance for us. 

    .img(v-if="isEjemploNico")  
      img(src='/static/ejemplo.png'  height="1500px")
    
    .espacioSegundo.left(v-if="isEjemploNico") NICOLAS:
      .letra The mayor of Cartagena has decided to consider your request concerning the elimination of Cabildos in Cartagena; however, due to social pressure he was forced to accept Miguel’s appeal that tries to stop Cabildos from being eradicated. You will have to present a letter in which you draft the reasons why Cabildos should be eliminated.

      .letra Use a formal register. Be clear and organized. You are the richest man in town, you can’t be defeated by your own slave. Here are some expressions the mayor considers relevant.
 


</template>

<script>
export default {
  name: 'app',

  data () {
    return {
      isMiguel: true,
      isNicolas: true,
      isEjemplo: false,
      isEjemploNico: false,

      isTexto1: false,
      isTexto1_1: false,
      isTexto1_2: false,
      isCuestionarioMiguel: false,

      isTexto2: false,
      isTexto2_1: false,
      isTexto2_2: false,
      isCuestionarioNicolas: false,

      resMig1: '',   
      resMig2: '',  
      resMig3: '',  
      resMig4: '', 
      resMig4_1: '', 
      resMig5: '',
      resMig6: '',

      resNic1: '',
      resNic2: '',
      resNic3: '',
      resNic3_1: '',
      resNic4: '',
      resNic5: '',
      resNic6: '',
      resNic6_1: '',

      isResMi1: true,
      isResMi2: true,
      isResMi3: true,
      isResMi4: true,
      isResMi4_1: true,
      isResMi5: true,
      isResMi6: true,
      
      isResNi1: true,
      isResNi2: true,
      isResNi3: true,
      isResNi3_1: true,
      isResNi4: true,
      isResNi5: true,
      isResNi6: true,
      isResNi6_1: true,

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
      this.isMiguel = false
      this.isTexto2 = true
      this.isTexto2_1 = true
      this.isTexto2_2 = true
      this.isCuestionarioNicolas = true
    },
    confirDatMig(){
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
      if (this.isResMi5 = (this.resMig5 == 'a good master' || this.resMig5 == 'benevolent'|| this.resMig5 == 'caring')) {
        this.contar++
      }
      if (this.isResMi6 =  this.resMig6 == 'treated better') {
        this.contar++ 
      }
      if (this.contar >= 4) {
        this.isEjemplo = true
      }
    },
  confirDatNic(){
    if (this.isResNi1 =  this.resNic1 == 'the owner' ) {
        this.contar++
      }
      if (this.isResNi2 = this.resNic2 == 'buy slaves') {
        this.contar++
      }
      if (this.isResNi3 =  (this.resNic3 == 'astonished' || this.resNic3 == 'amazed'|| this.resNic3 == 'shocked')) {
        this.contar++
      }
      if (this.isResNi3_1 = (this.resNic3_1 == 'bad appearance' || this.resNic3_1 == 'dirt' || this.resNic3_1 == 'filthiness')) {
        this.contar++
      }
      if (this.isResNi4 = (this.resNic4 == 'flawless' || this.resNic4 == 'in perfect conditions')) {
        this.contar++
      } 
      if (this.isResNi5 = (this.resNic5 == 'good master' || this.resNic5 == 'good person')) {
        this.contar++
      }
      if (this.isResNi6 = (this.resNic6 == 'rebels' || this.resNic6 == 'cocky' || this.resNic6 == 'arrogant')) {
        this.contar++ 
      }
      if (this.isResNi6_1 = (this.resNic6_1 == 'worried' || this.resNic6_1 == 'concerned' )) {
        this.contar++ 
      }
      if (this.contar >= 5) {
        this.isEjemploNico = true
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
  
  .espacioPrimero
    margin-top 20px
  
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

  .espacioSegundo
    margin 40px 0px 10px

</style>
