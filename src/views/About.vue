<template>
  <div class="about">
    <HelloAbout header="Vette shit :-)">This is an about page</HelloAbout>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloAbout from '@/components/HelloAbout.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloAbout,
  },
})
export default class About extends Vue {}
</script>
