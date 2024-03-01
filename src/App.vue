<template>
  <SearchBar @termChange="onTermChange" />
</template>

<script>
import SearchBar from './components/SearchBar.vue';
import axios from 'axios';

const API_KEY = 'AIzaSyDuK1U6c8JkvyTBJ44fhgZDz5skj3SRORk';

export default {
  name: 'App',
  components: {
    SearchBar
  },
  methods: {
    onTermChange(searchTerm) {
      console.log('app component: ', searchTerm);
      axios.get('https://googleapis.com/youtube/v3/search', {
        params: {
          key: API_KEY,
          type: 'video',
          part: 'snippet',
          q: searchTerm
        }
      }).then(response => console.log(response))
    }
  }
}
</script>

<style>
</style>
