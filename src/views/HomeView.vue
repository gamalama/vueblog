<template>
  <div class="home">
    <p>Hi, I'm {{ name }}. This is my  number {{ number }}</p>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  setup() {
    // console.log('setup')
    // Tidak reaktif
    const name = "Fakhry";
    const number = "01234";

    return {
      // name: name,
      // number: number,
      name,
      number,
    }
  },
  // created() {
  //   console.log('created')
  // },
  // mounted() {
  //   console.log('mounted')
  // }
}
</script>
