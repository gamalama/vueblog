<template>
  <div class="home">
    <p ref="p">Hi, I'm {{ name }}. This is my number {{ number }}</p>
    <button @click="handleClick">Click!</button>
  </div>
</template>

<script>

import {ref} from "vue";

export default {
  name: 'HomeView',
  setup() {
    const p = ref(null);
    const name = "Fakhry";
    const number = "01234";

    const handleClick = () =>{
      console.log(p, p.value);
      p.value.classList.add('paragraph');
      p.value.textContent = "hi, Codepolitan"
    }

    return {
      name,
      number,
      p,
      handleClick,
    }
  },
}
</script>
