<template>
  <div class="container">

      <canvas>
      </canvas>

  </div>
</template>

<script lang="ts">
import { Prop, Vue, Component } from 'vue-property-decorator';

@Component
export default class GameComponent extends Vue {
}
</script>

<style lang="scss" scoped>
.container {
    padding: 20px 30px 20px 30px;
    canvas {
        width: 1280px;
        height: 768px;
        background-color: #000;
        box-shadow: 0px 0px 4px 10px rgba(0,0,0,.3);
    }
}
</style>
