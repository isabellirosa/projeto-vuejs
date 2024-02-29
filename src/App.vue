
<template>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p >Valor do contador é: {{ contador }}</p>
  <button @click="zerar">Zerar</button>
</template>

<style scoped>
button {
  font-weight: bold;
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
