<template>
  <div class="container">
    <h1>Welcome to the Nuxt test app!</h1>
    <a-alert message="We are using antd design system." type="info" show-icon />
    <ul>
      <li>Click <nuxt-link to="/section-one">here</nuxt-link> to enter in the section one.</li>
      <li>Click <nuxt-link to="/section-two">here</nuxt-link> to enter in the section two.</li>
    </ul>
    <a-alert message="Enjoy the ride!" type="success" show-icon />
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  head: {
    title: 'Nuxt Test - Home page'
  },
  data() {
    return {}
  },
});
</script>

<style>
/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
