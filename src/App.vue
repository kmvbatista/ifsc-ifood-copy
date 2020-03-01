<template>
  <div class="main">
    <headerApp></headerApp>
    <router-view></router-view>
  </div>
</template>

<script>
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    headerApp: Header,
  },
};
</script>

<style></style>
