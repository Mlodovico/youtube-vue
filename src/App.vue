<script>
import axios from 'axios';

import HeaderComponent from './components/HeaderComponent.vue'
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    Card
  },
  data() {
    return {
      videos: []
    }
  },
  mounted() {
    this.getVideoData();
  },
  methods: {
    async getVideoData() {
      try {
        const response = await axios.get('http://localhost:3000/video');
        this.videos = response.data;
      } catch (error) {
        console.log('Error:', error);
      }
    }
  }
}
</script>

<template>
  <HeaderComponent />
  <div class="card-wrapper">
    <Card v-bind="video" v-for="video in videos" :key="video" :video="video" />
  </div>

</template>
<style scoped>
.card-wrapper {
  display: flex;

  height: auto;
  flex-wrap: wrap;
}

.card-wrapper .card {
  flex: 1 1 calc(33.333% - 32px);
  max-width: 200px;
}
</style>
