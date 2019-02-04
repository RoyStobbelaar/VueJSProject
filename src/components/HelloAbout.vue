<template>
  <div class="container">
      <div class="container-header">
          {{ header }}
      </div>

      <div class="container-body">
          Dit is nu een about component geworden! <br>
          Eerste Vue component! Yeaaah!
      </div>

  </div>
</template>

<script lang="ts">

import { Prop, Vue, Component } from 'vue-property-decorator';

@Component
export default class HelloAbout extends Vue {
    @Prop() header!: string;
}

</script>

<style lang="scss" scoped>

.container {
    padding: 20px 30px 20px 30px;
    .container-header {
        font-size: 28px;
    }
    .container-body {
        font-size: 20px;
        background-color: #ddd;
        border: 2px solid #333;
        border-radius: 24px;
        box-shadow: 1px 2px 4px 8px rgba(0,0,0,.4);
        height: 400px;
    }
}

</style>
