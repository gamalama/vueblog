<template>
  <div class="home">
    <h2>Ref</h2>
    <p>Hi, I'm {{ contactOne.name }}. This is my number {{ contactOne.number }}</p>
    <button @click="handleClick">Click!</button>
    <h2>Reactive</h2>
    <p>Hi, I'm {{ contactTwo.name }}. This is my number {{ contactTwo.number }}</p>
    <button @click="handleClickTwo">Click!</button>
  </div>
</template>

<script>

import {reactive, ref} from "vue";

export default {
  name: 'HomeView',
  setup() {
    const contactOne = ref({
      name: 'Fakhry',
      number: '0123456',
    })

    const contactTwo = reactive({
      name: 'Affan',
      number: '0654321',
    })

    const handleClick = () => {
      contactOne.value.name = "Linux";
      contactOne.value.number = "007";
    }

    const handleClickTwo = () => {
      contactTwo.name = "Arsene";
      contactTwo.number = "001";
    }

    return {
      contactOne,
      contactTwo,
      handleClick,
      handleClickTwo,
    }
  },
}
</script>
