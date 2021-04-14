<template>
  <div class="home">
    <h1>arek blog</h1>
    <p ref="par">My name is {{ name }} and my age is {{ age }}.</p>
    <button @click="handleClick">Click</button>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Home",
  setup() {
    console.log("setup");

    const par = ref(null);
    console.log(par, par.value);

    let name = "Arek";
    let age = 35;

    const handleClick = () => {
      console.log(par, par.value);
      par.value.classList.add("test");
      par.value.textContent = "hello world";
    };

    return { name, age, handleClick, par };
  },
};
</script>
