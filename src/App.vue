
<template>
  <div>
  <button @click="incrementarContador">+</button>
  <p > {{ contador }}</p>
  <button  @click="decrementarContador">-</button>
  <button @click="zerar">Zerar</button>
  </div>
</template>

<style scoped>
button {
  background-color: rgb(231, 230, 255);
  border-radius: 8px;
   border: 1px solid black;
   margin: 5px;
} 
div{
  display: flex; 
  align-items: center;
   justify-content: center;
    }
/*API de opções:*/
</style>

<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador(){
    if(this.contador>0)this.contador--
    },
    zerar(){
    this.contador=0
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
 </script>
<!-- API de composição:
   <script setup>
import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if(contador.value>0)contador.value--
}
zerar(){
    contador.value=0
    }

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script> -->
