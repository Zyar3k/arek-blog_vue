<template>
  <div class="home">
    <h1>arek blog</h1>
    <p>My name is {{ name }} and my age is {{ age }}.</p>
    <button @click="handleClick">Click</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  setup() {
    console.log("setup");

    let name = "Arek";
    let age = 35;

    const handleClick = () => {
      console.log("clicked");
    };

    return { name, age, handleClick };
  },
};
</script>
