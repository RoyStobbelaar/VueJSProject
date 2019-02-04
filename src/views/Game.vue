<template>
    <div class='container'>
        <GameComponent></GameComponent>
    </div>
</template>

<script lang="ts">

import { Component, Vue } from 'vue-property-decorator';
import GameComponent from '@/components/GameComponent.vue'; // @ is an alias to /src

@Component({
components: {
    GameComponent,
    },
})
export default class Game extends Vue {}
</script>