<template>
  <div class="home">
    <h1>arek blog</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="handleClick">toggle post</button>
    <button @click="posts.pop()">delete post</button>
  </div>
</template>

<script>
import PostList from "../components/PostList";
import { ref } from "vue";
export default {
  name: "Home",
  components: { PostList },
  setup() {
    const posts = ref([
      {
        title: "Welcome to the blog",
        body:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam aliquid modi eos tempore maiores, labore quisquam eum consectetur suscipit hic! Minima sunt aliquid quae assumenda beatae vitae eaque numquam, tempora quas ab ex blanditiis reprehenderit minus nesciunt adipisci excepturi temporibus alias sapiente, quia facilis, necessitatibus dolore. Saepe, provident vitae, non ut est alias excepturi amet perferendis facere vel, nostrum laudantium hic dolorem ullam quasi repudiandae accusamus voluptas consequatur? Incidunt dolore nesciunt repellendus aut maiores maxime voluptatum sunt, rem eius, repudiandae laboriosam quasi totam, deserunt ea facilis similique beatae vero delectus perferendis ullam. Repudiandae non quo, sint laborum fugiat quia consectetur.",
        id: 1,
      },
      {
        title: "Top 5 css tips",
        body:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam aliquid modi eos tempore maiores, labore quisquam eum consectetur suscipit hic! Minima sunt aliquid quae assumenda beatae vitae eaque numquam, tempora quas ab ex blanditiis reprehenderit minus nesciunt adipisci excepturi temporibus alias sapiente, quia facilis, necessitatibus dolore. Saepe, provident vitae, non ut est alias excepturi amet perferendis facere vel, nostrum laudantium hic dolorem ullam quasi repudiandae accusamus voluptas consequatur? Incidunt dolore nesciunt repellendus aut maiores maxime voluptatum sunt, rem eius, repudiandae laboriosam quasi totam, deserunt ea facilis similique beatae vero delectus perferendis ullam. Repudiandae non quo, sint laborum fugiat quia consectetur.",
        id: 2,
      },
    ]);

    const showPosts = ref(true);

    const handleClick = () => {
      showPosts.value = !showPosts.value;
    };

    return { posts, showPosts, handleClick };
  },
};
</script>
