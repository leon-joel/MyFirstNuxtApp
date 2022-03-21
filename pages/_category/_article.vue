<template>
  <h1>{{ this.$route.params.category }}/{{ this.$route.params.article }}</h1>
</template>

<script>
export default {
  // サーバー側とクライアント側で実行
  created() {
    console.log('created');
    console.log(this.$route);
  },

}
</script>

<style>

</style>
