<template>
  <div>
    <h1>記事一覧</h1>
    <!-- <p v-if="$fetchState.pending">Fetching posts...</p> -->
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
    };
  },
  // mountedフック ※必ずクライアントサイドでデータを取得する
  async mounted() {
    const posts = await this.$axios.$get(
      "https://jsonplaceholder.typicode.com/posts/"
    );
    this.posts = posts;
  },

  // // fetchフック
  // async fetch() {
  //   const posts = await this.$axios.$get(
  //     "https://jsonplaceholder.typicode.com/posts/"
  //   );
  //   this.posts = posts;
  // },
  // fetchOnServer: false,

  // // asyncDataフック
  // async asyncData({ $axios }) {
  //   const posts = await $axios.$get(
  //     "https://jsonplaceholder.typicode.com/posts/"
  //   );
  //   return { posts };
  // },
};
</script>
