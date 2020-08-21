<template>
  <div class="container">
    <h1>Welcome to the Nuxt test app</h1>
    <h2>This is the section two page</h2>
    <a-alert message="We are using antd design system." type="info" show-icon />
    <nuxt-link to="/">Home page</nuxt-link>
    <a-alert message="Enjoy the ride!" type="success" show-icon />
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  head: {
    title: 'Nuxt Test - Section two'
  },
  data() {
    return {}
  },
});
</script>

<style>

</style>
