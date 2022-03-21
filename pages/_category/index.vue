<template>
  <h1>カテゴリー:{{ this.$route.params.category }}</h1>
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
