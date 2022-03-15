<template>
     <div class="escena">
    <p>{{escena}}</p>
  </div>
</template>



<script>
export default {
  name: 'Escena',
  props: {
    escena: String,
  }
}

</script>



<style>
.escena {
    margin: 1rem;
    border-radius: 5rem;
    border: 2px solid black;
    text-align: center;
}
</style>