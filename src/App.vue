<script>
import axios from 'axios';

import HeaderComponent from './components/layout/HeaderComponent.vue'
import Card from './components/common/Card.vue';

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
  <div class="card-conteiner">
    <Card v-bind="video" v-for="video in videos" :key="video" :video="video" />
  </div>

</template>
<style scoped>
.card-conteiner {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  width: 100%;
  margin: 0 auto;

  @media screen and (width >=1366px) {
    grid-template-columns: repeat(4, 1fr);
  }

  @media screen and (width <=900px) {
    grid-template-columns: repeat(2, 1fr);
  }

  @media screen and (width <=600px) {
    grid-template-columns: repeat(1, 1fr);
    gap: 10px;
  }
}

.card-wrapper .card {
}
</style>
