<script setup>
import { ref } from 'vue'
import Versions from './components/Versions.vue'

const ipcHandle = () => window.electron.ipcRenderer.send('ping')

const count = ref(0)
</script>

<template>
  <img alt="logo" class="logo" src="./assets/electron.svg" />
  <!-- <div class="creator">Powered by electron-vite</div> -->
  <!-- <div class="text">
    Build an Electron app with
    <span class="vue">Vue</span>
  </div> -->
  <!-- <p class="tip">Please try pressing <code>F12</code> to open the devTool</p> -->
  <div>
    <button @click="count--" style="cursor: pointer;">-</button>
    {{ count }}
    <button @click="count++" style="cursor: pointer;">+</button>
  </div>
  <div class="actions">
    <!-- <div class="action">
      <a href="https://electron-vite.org/" target="_blank" rel="noreferrer">Documentation</a>
    </div> -->
    <!-- <div class="action">
      <a target="_blank" rel="noreferrer" @click="ipcHandle">Send IPC</a>
    </div> -->
  </div>
  <!-- <Versions /> -->
</template>
