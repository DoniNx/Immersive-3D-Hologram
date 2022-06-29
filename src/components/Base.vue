<script setup>
import { ref } from 'vue'

const props = defineProps({
  playAudio: Boolean
});


</script>

<template>
  <video src="../assets/vid-file.mp4" v-bind:muted="!props.playAudio" loop autoplay></video>
</template>

<style scoped>

*{
  background: transparent;
}


</style>
