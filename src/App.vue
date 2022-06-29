<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Base from './components/Base.vue'
import { ref } from 'vue'



var showVid = ref(false);

function spinnerTime(params) {
  setTimeout(() => {
    showVid.value = true;
  }, 36000);
}
spinnerTime();

</script>

<template>
  
  <Base v-show="showVid" class="Base" :playAudio="showVid" />
  <div class="loadingPage" v-show="!showVid">
  
  <div class="flower-container">
<div class="flower-spinner">
  <div class="dots-container">
    <div class="bigger-dot">
      <div class="smaller-dot"></div>
    </div>
  </div>
</div>
<br />
  <p >Loading content ...</p>
  
  </div>
</div>


</template>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: rgb(2, 32, 44);
}
.Base{
  height: 100vh;
  max-width: 400px;

  margin: 0 auto;
  color:blue;
}

.flower-spinner,  .flower-spinner * {
      box-sizing: border-box;
    }

    .flower-spinner {
      height: 70px;
      width: 70px;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
    }

    .flower-spinner .dots-container {
      height: calc(70px / 7);
      width: calc(70px / 7);
    }

    .flower-spinner .smaller-dot {
      background: #ff1d5e;
      height: 100%;
      width: 100%;
      border-radius: 50%;
      animation: flower-spinner-smaller-dot-animation 2.5s 0s infinite both;

    }

    .flower-spinner .bigger-dot {
      background: #ff1d5e;
      height: 100%;
      width: 100%;
      padding: 10%;
      border-radius: 50%;
      animation: flower-spinner-bigger-dot-animation 2.5s 0s infinite both;
    }

    @keyframes flower-spinner-bigger-dot-animation {
      0%, 100% {
        box-shadow: rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px;
      }

      50% {
        transform: rotate(180deg);
      }

      25%, 75% {
        box-shadow: rgb(255, 29, 94) 26px 0px 0px,
        rgb(255, 29, 94) -26px 0px 0px,
        rgb(255, 29, 94) 0px 26px 0px,
        rgb(255, 29, 94) 0px -26px 0px,
        rgb(255, 29, 94) 19px -19px 0px,
        rgb(255, 29, 94) 19px 19px 0px,
        rgb(255, 29, 94) -19px -19px 0px,
        rgb(255, 29, 94) -19px 19px 0px;
      }

      100% {
        transform: rotate(360deg);
        box-shadow: rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px;
      }
    }

    @keyframes flower-spinner-smaller-dot-animation {
      0%, 100% {
        box-shadow: rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px;
      }

      25%, 75% {
        box-shadow: rgb(255, 29, 94) 14px 0px 0px,
        rgb(255, 29, 94) -14px 0px 0px,
        rgb(255, 29, 94) 0px 14px 0px,
        rgb(255, 29, 94) 0px -14px 0px,
        rgb(255, 29, 94) 10px -10px 0px,
        rgb(255, 29, 94) 10px 10px 0px,
        rgb(255, 29, 94) -10px -10px 0px,
        rgb(255, 29, 94) -10px 10px 0px;
      }

      100% {
        box-shadow: rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px,
        rgb(255, 29, 94) 0px 0px 0px;
      }
    }

    .loadingPage{
      display: flex;
      flex-direction: column;
      
      height: 100vh;
      color: white;

    }
    .flower-container{
      margin: auto auto;
    }
    .flower-spinner{
      margin: auto auto;
    }

</style>
