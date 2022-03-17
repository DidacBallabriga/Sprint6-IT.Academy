<template>
      <Benvinguda @start="benvinguda" v-if="start"></Benvinguda>
    <div class="container" v-else>
      <Botons @prev="recivePrev" @seg="reciveSeg"></Botons>
      <Escena :text="textos" :activeSentence="currentSentence"></Escena>
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
  style: {
          backgroundImage: "url(../uploads/portadaVue6.png)",
          backgroundRepeat: "no-repeat",
          backgroundSize: "cover"
        },
  data(){
    return {
      textos: ["El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial", "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.","L'heroi va decidir travessar la porta que el portava a casa","Mentrestant, altres heroes no van tenir tanta sort en la seva elecció..."],
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
          this.currentSentence++
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
