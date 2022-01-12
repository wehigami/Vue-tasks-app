<template>
  <div class="home">
    <Nav brand="Wehi Tasks"/>
    <Tasks/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Nav from '@/components/Navbar.vue';
import Tasks from '@/components/Tasks.vue';

@Component({
  components: {
    Nav,
    Tasks
  },
})
export default class Home extends Vue {}
</script>

<style scoped>
</style>
