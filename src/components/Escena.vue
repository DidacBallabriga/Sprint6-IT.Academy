<template>
     <div class="frases">
        <p 
          v-for = "(texto,i) in text" 
          :key="i"
          :class="{active: i === activeSentence}"> 
          {{ texto.txt }}
        </p>
  </div>
</template>


<script>
export default {
  name: 'Escena',
  props: ['text','activeSentence']
}

</script>


<style scoped>

p {
    padding: 1rem;
    margin: 1rem;
    border-radius: 5rem;
    border: 2px solid black;
    text-align: center;
}
.active {
  background-color: #ffc0cb;
}
</style>>