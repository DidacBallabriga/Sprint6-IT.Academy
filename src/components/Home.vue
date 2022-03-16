<template>
    <div class="container">
      <Botons @prev="recivePrev" @seg="reciveSeg"></Botons>
      <Escena :text="textos" :activeSentence="currentSentence"></Escena>
    </div>
</template>

<script>
import Escena from './Escena.vue';
import Botons from './Botons.vue';

export default {
  name: 'Home',
  components: {
    Escena,
    Botons
  },
  data(){
    return {
      textos: ["El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial", "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.","L'heroi va decidir travessar la porta que el portava a casa","Mentrestant, altres heroes no van tenir tanta sort en la seva elecció..."],
      currentSentence: 0
      }
    },
    methods: {
      recivePrev(prev){
        if(this.currentSentence >= 1){
        this.currentSentence--
        }
      },
       reciveSeg(num){
         if(this.currentSentence < (this.textos.length-1)){
          this.currentSentence++
         }
      }
    }
} 
</script>



<style>

</style>
