<template>
  <div class="home">
    <h1>Home</h1>
    <!--    <div>{{ name }}</div>-->
    <input type="text" v-model="search">
    <div v-for="name in resultSearch" :key="name">
      {{ name }}
    </div>
  </div>
</template>

<script>

import {computed, ref} from "vue";

export default {
  name: 'HomeView',
  setup() {
    // const name = computed(() => {
    //   return 'Fakhry';
    // });
    const search = ref('');
    const names = ref([
      'Katlyn Lehmann', 'Darwin Tremaine', 'Noriko Stgelais',
      'Shawna Fairbank', 'Zachery Raap', 'Ahmad Urenda',
      'Raymon Lafrance', 'Carolyn Bolander', 'Sharell Satcher',
      'Annett Purcell'
    ]);

    const resultSearch = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });

    return {
      names,
      search,
      resultSearch,
    }
  },
}
</script>
