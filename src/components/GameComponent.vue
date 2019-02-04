<template>
  <div class="container">

      <canvas id="myCanvas" @click="someMethod" ref="canvas">
      </canvas>

  </div>
</template>

<script lang="ts">
import { Prop, Vue, Component } from 'vue-property-decorator';

@Component
export default class GameComponent extends Vue {

$refs:any = {
    canvas: HTMLCanvasElement
  }

  canvas: any;
  ctx: any;
  x: number = 0;
  y: number = 0;
  height: number = 768;
  width: number = 1280;

  someMethod () {
    console.log('click!');
    this.canvas = this.$refs.canvas;
    this.canvas.width = this.width;
    this.canvas.height = this.height;

    this.ctx = this.$refs.canvas.getContext("2d");
    this.ctx.fillStyle = "#fff";
    this.ctx.fillRect(this.x,this.y,this.width, this.height);
  }

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
