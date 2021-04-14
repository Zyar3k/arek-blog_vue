<template>
  <div class="home">
    <h1>arek blog</h1>
    <p>My name is {{ name }} and my age is {{ age }}.</p>
    <button @click="handleClick">Click</button>
    <button @click="age++">Plus age</button>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Home",
  setup() {
    // const par = ref(null);

    const name = ref("Arek");
    const age = ref(35);

    const handleClick = () => {
      console.log("handleClick");
      name.value = "czarek";
      age.value = 53;
    };

    return { name, age, handleClick };
  },
};
</script>
