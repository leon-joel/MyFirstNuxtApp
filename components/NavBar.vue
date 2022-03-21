<template>
  <div>
    <nav>
      <!-- nuxt-linkタグをrouter-linkタグに変更しても動作します。
      nuxt-linkでは後ほど出てくるprefetchの機能があります。
      ページを開かなくても先にそのページのJavaScriptファイルをFetch(取得)しておく機能です。
      またaタグに変更しても動作はしますが、
      リンクをクリックする度にブラウザのリロードが行われページを構成するすべての情報をリロード毎に取得します。
      通常のHTMLページ間での移動と同じ動作になります。 -->
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/about" no-prefetch>About</nuxt-link>
      <nuxt-link :to="{ name: 'users-list'}" no-prefetch>UserList</nuxt-link>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
