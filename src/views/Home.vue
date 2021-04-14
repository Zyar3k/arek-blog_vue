<template>
  <div class="home">
    <h1>arek blog</h1>
    <h2>refs</h2>
    <p>{{ userOne.name }} - {{ userOne.age }}</p>
    <button @click="updateUserOne">Update user one</button>
    <h2>reactive</h2>
    <p>{{ userTwo.name }} - {{ userTwo.age }}</p>
    <button @click="updateUserTwo">Update user two</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "Home",
  setup() {
    // const par = ref(null);

    const userOne = ref({ name: "Arek", age: "35" });
    const userTwo = reactive({ name: "Marek", age: "25" });

    // ref are better ;)

    const updateUserOne = () => {
      userOne.value.age = 36;
    };
    const updateUserTwo = () => {
      userTwo.age = 28;
    };

    return { userOne, updateUserOne, userTwo, updateUserTwo };
  },
};
</script>
