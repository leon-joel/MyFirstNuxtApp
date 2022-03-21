<template>
  <h1>ユーザID: {{ this.$route.params.id }}, name: {{ user.name }}</h1>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
      users: [
        {
          id: 1, name: 'John Doe'
        },
        {
          id: 2, name: 'Kevin Smith',
        },
        {
          id: 3, name: 'Harry Bosch'
        },
      ],
    }
  },
  computed: {
    user() {
      return this.users.find(user => user.id == this.id);
    }
  },

  // サーバー側とクライアント側で実行
  created() {
    console.log('created');
    console.log(this.$route);
  },
  // クライアントだけで実行
  mounted() {
    console.log('mounted');
    console.log(this.$route);
  }
}
</script>

<style>
</style>
