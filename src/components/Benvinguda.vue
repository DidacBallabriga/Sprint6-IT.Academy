<template>
  <div class="container">
    <img src="../assets/portadaVue6.png" alt="">
    <button @click="$emit('start')">COMENÇAR</button>
  </div>

</template>

<script>
export default {
  name: 'Benvinguda'
}
</script>


<style scoped>
.container {
    width: 100%;
    padding-left: 15px;
    padding-right: 15px;
    margin-left: auto;
    margin-right: auto;
    max-width: 1280px;
    display: flex;
}
img{  
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    text-align: center;
    width: 40%;
    z-index: 10;
    top: -2rem;
}
button {
  background-color: #ce05ce;
  font-size: 1.5rem;
  font-weight: 800;
  width: 15rem;
  height: 3.5rem;
  border: 8px solid rgb(0, 0, 0);
  border-radius: 5rem;
  cursor: pointer;
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  top: 60%;
  text-align: center;
  z-index: 20;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  letter-spacing: 0.2rem;
}
@media (max-width: 1024px){
  button{
  top: 60%;
  }  
}
@media (max-width: 768px){
  button{
  width: 10rem;
  height: 2.5rem;
  font-size: 1rem;
  border: 6px solid rgb(0, 0, 0);
  top: 60%;
  }  
}
@media (max-width: 425px){
  img{  
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    text-align: center;
    width: 80%;
    z-index: 10;
}
}
@media (max-width: 375px){
 button{
  top: 40%;
  } 
}
button::before {
content: '';
  border-radius: 1000px;
  min-width: calc(250px + 12px);
  min-height: calc(50px + 12px);
  border: 6px solid #ce05ce;
  box-shadow: 0 0 60px #ce05ce;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: all .3s ease-in-out 0s;
}
.button:hover, .button:focus {
  color: #313133;
  transform: translateY(-6px);
}
button:hover::before, button:focus::before {
  opacity: 1;
}

button::after {
  content: '';
  width: 30px; height: 30px;
  border-radius: 100%;
  border: 6px solid #ce05ce;
  position: absolute;
  z-index: -1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: ring 1.5s infinite;
}

button:hover::after, button:focus::after {
  animation: none;
  display: none;
}

@keyframes ring {
  0% {
    width: 30px;
    height: 30px;
    opacity: 1;
  }
  100% {
    width: 300px;
    height: 300px;
    opacity: 0;
  }
}

</style>