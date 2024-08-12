<script>
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
      videoData: {
        title: 'Como fazer bolo de cenoura',
        author: 'Murilo Lodovico',
        description: 'Lorem ipsum'
      }
    }
  }
}
</script>

<template>
  <HeaderComponent />

  <Card :video="videoData" />

</template>

<style scoped></style>
