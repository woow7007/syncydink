<template>
  <div>
    <v-layout class="videojs-container" column align-center>
      <v-flex>
        <video-player
          class="vjs-big-play-centered"
          id="videojs-player"
          ref="videoPlayer"
          :options="playerOptions"
          @play="onPlayerPlay($event)"
          @pause="onPlayerPause($event)"
          @canplay="onPlayerReady($event)"
          @loadeddata="onPlayerReady($event)">
        </video-player>
      </v-flex>
      <v-flex v-if="this.vrMode">
        <aframe-video-player
          :currentPlayer="this.currentPlayer">
        </aframe-video-player>
      </v-flex>
    </v-layout>
  </div>
</template>

<style lang="css">
 #videojs-player {
   display: flex;
   max-width: 100vw;
 }
</style>

<script lang="ts" src="./VideoPlayer.ts">
</script>

<style src="video.js/dist/video-js.min.css" lang="css">
</style>

<style src="vue-video-player/src/custom-theme.css" lang="css">
</style>
