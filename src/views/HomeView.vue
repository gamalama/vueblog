<template>
  <div class="home">
    <p>Hi, I'm {{ name }}. This is my number {{ number }}</p>
    <button @click="handleClick">Click!</button>
    <button @click="number++">Increment</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>

import {ref} from "vue";

export default {
  name: 'HomeView',
  setup() {
    const name = ref("Fakhry");
    const number = ref("01234");

    const handleClick = () => {
      name.value = "Linux";
      number.value = "007";
    }

    return {
      name,
      number,
      handleClick,
    }
  },
}
</script>
