<template lang='pug'>
  .app
    .texto1(v-if="is1" @click="choose(1, 1)") T1 {{ st1 }}
    .texto2(v-if="is2" @click="choose(2, 2)") T2 {{ st2 }}
    .texto3(v-if="is3" @click="choose(1, 3)") T3 {{ st3 }}
    .texto4(v-if="is4" @click="choose(2, 4)") T4 {{ st4 }}

</template>

<script>
export default {
  name: 'app',

  data () {
    return {
      msg: 'El primer mensaje',
      t1: ['texto11', 'trxto 12'],
      t11: ['texto111', 'trxto 112'],
      t2: ['texto21', 'trxto 22'],
      st1: 'texto1',
      st2: 'trxto 2',
      st3: '',
      st4: '',
      is1: true,
      is2: true,
      is3: false,
      is4: false,
      line: '',
      count: 0
    }
  },

  methods:{
    choose(pos, texto){

      this.is2 = !this.is2
      this.is1 = !this.is1
      this.is3 = !this.is3
      this.is4 = !this.is4

      
      const nRespuesta = this[`t${this.line}${pos}`]
      console.log(nRespuesta)

        this.line = this.line + String(pos)

      if(texto == 1 || texto == 2){
        this.st3 = nRespuesta[0]
        this.st4 = nRespuesta[1]
      } else {
        this.st1 = nRespuesta[0]
        this.st2 = nRespuesta[1]
      }
  
    }
  }
}
</script>

<style lang='stylus'>
  .app

  .textoDercha
    text-align center

</style>
