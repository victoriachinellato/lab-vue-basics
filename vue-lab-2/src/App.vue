<template>
  <NavBar />

  <div>
    <h1>Iteracion 2:</h1>
    <div>Operation with js: {{2 + 2}}</div>
    <div>This is: {{showString()}}</div>
  </div>


  <div>
    <h1>Iteracion 3: Show an element only if a particular property is set to true</h1>
    <div v-if="condition1">Condition 1 is true</div>
    <div v-else-if="condition2">Condition 2 is true and 1 is false</div>
    <div v-else>Condition 1 and condition 2 are flase </div>
  </div>


  <div>
    <h1>Iteracion 4: Display a list of elements that are stored inside a component </h1>
    <div v-for="element in elements" :key="element"> {{element}}</div>
  </div>

  <div>
    <h1>Bonus: Change the background color of an element when pressing a button</h1>
    <button @click="changeBackground()">Click me!</button>
    <div id="divToChange">Press the buttom to change background</div>

  </div>

  <Footer />
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'

import { ref } from 'vue'

// para iteracion 2:
const showString = () => {
    const myString = 'Inserting strings with js'
    return myString;
}

// para iteracion 3:

const condition1 = ref(true)
const condition2 = ref(true)

// para iteracion 4:

const elements = ['element1', 'element2', 'element3', 'element4']


// para bonus

// const changeBackground = () => {
//   const backgroundB = 
  
   

  

  
// }


</script>
<style scoped>

.background {
  background-color: blueviolet;
}
</style>