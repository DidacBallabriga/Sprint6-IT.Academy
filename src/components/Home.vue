<template>
      <Benvinguda @start="benvinguda" v-if="false"></Benvinguda>
    <div class="container" v-else :style="{ backgroundImage: `url(${textos[currentSentence].img})`}">
      <Botons @prev="recivePrev" @seg="reciveSeg"></Botons>
      <Escena :text="textos" :activeSentence="currentSentence"></Escena>
      <img src="../assets/1.jpg" alt="">

     
    </div>
</template>

<script>
import Benvinguda from './Benvinguda.vue';
import Escena from './Escena.vue';
import Botons from './Botons.vue';

export default {
  name: 'Home',
  components: {
    Benvinguda,
    Escena,
    Botons
  },
  data(){
    return {
      textos: [{txt: "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial", imga:"1.jpg"},
      {txt: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.", img:require("../assets/2.jpg")},
      {txt: "L'heroi va decidir travessar la porta que el portava a casa", img:require("../assets/3.jpg")},
      {txt: "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció...", img:require("../assets/4.jpg")}],
      currentSentence: 0,
      start: true
      }
    },
    methods: {
      recivePrev(currentSentence){
        if(this.currentSentence >= 1){
        this.currentSentence--
        }
      },
       reciveSeg(currentSentence){
         if(this.currentSentence < (this.textos.length-1)){
          this.currentSentence++;
         }
      },
      benvinguda(start){
        this.start = false;
      }
    }
} 
</script>



<style>


</style>
