<template>
  <div class="about">
    <div id="nav">
      <router-link to="/">Home</router-link>
    </div>
    <router-view/>
    <h1>This is an about page</h1>
    <h2>hello</h2>
    <Tasks/>
  </div>
</template>
<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';
  import Tasks from '@/components/Tasks.vue';

  @Component({
    components: {
      Tasks
    },
  }) 

  export default class About extends Vue {}
</script>

