<template>
  <SearchBar @termChange="onTermChange" />
</template>

<script>
import SearchBar from './components/SearchBar.vue';

export default {
  name: 'App',
  components: {
    SearchBar
  },
  methods: {
    onTermChange(searchTerm) {
      console.log('app component: ', searchTerm);
    }
  }
}
</script>

<style>
</style>
