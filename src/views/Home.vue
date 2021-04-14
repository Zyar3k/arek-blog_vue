<template>
  <div class="home">
    <h1>arek blog</h1>
    <input type="text" v-model="search" />
    <p>search term: {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">
      {{ name }}
    </div>
  </div>
</template>

<script>
import { computed, ref } from "vue";
export default {
  name: "Home",
  setup() {
    const search = ref("");
    const names = ref(["arek", "czarek", "marek", "darek", "jarek"]);

    const matchingNames = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });
    return { names, search, matchingNames };
  },
};
</script>
