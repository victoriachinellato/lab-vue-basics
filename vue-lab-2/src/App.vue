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
    <!-- <div v-else-if="condition2">Condition 2 is true and 1 is false</div> -->
    <!-- <div v-else>Condition 1 and condition 2 are flase </div> -->
    <button @click="changeCondition1()">change condition 1</button>
  </div>


  <div>
    <h1>Iteracion 4: Display a list of elements that are stored inside a component </h1>
    <div v-for="element in elements" :key="element"> {{element}}</div>
  </div>
  <br />

  <div>
    <h1>Bonus: Change the background color of an element when pressing a button</h1>
    <button @click="onClick()">Click me!</button>
    <div :class="{background: changeBackground}">Press the buttom to change this background</div>
  </div>
  <br />


  <div>
    <h1>Iteracion extra: mostrar en el div de abajo el input</h1>
    <!-- v-model sirve para guardar input y mostrarlo -->
    <input type="text" v-model="inputValue">
    <div>{{inputValue}}</div>
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

const changeCondition1 = () => {
  condition1.value = !condition1.value
}
const condition2 = ref(true)

// para iteracion 4:

const elements = [
        {
        title: 'Titulo 1',
        description: 'Description 1',
        content: 'Content 1',
        },
        {
        title: 'Titulo 2',
        description: 'Description 2',
        content: 'Content 2',
        },
        {
        title: 'Titulo 3',
        description: 'Description 3',
        content: 'Content 3',
        },
]


// para bonus

const changeBackground = ref(false)
const onClick = () => {
  changeBackground.value = !changeBackground.value
}

// const changeBackground = () => {
//   const backgroundB = 
  
   
// iteracion extra

const inputValue = ref();

  

  
// }


</script>
<style scoped>

.background {
  background-color: blueviolet;
}
</style>