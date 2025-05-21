<template>
  <button id="bouncy-btn" @click="$emit('scrollTo', 'presentacion')">
    <span class="material-symbols-outlined">keyboard_arrow_down</span>
  </button>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const btn = document.getElementById('bouncy-btn')
  let dir = 1
  let pos = 0

  setInterval(() => {
    if (pos >= 20) dir = -1
    if (pos <= 0) dir = 1
    pos += dir
    btn.style.transform = `translateY(${pos}px)`
  }, 60)
})
</script>

<style scoped>
#bouncy-btn {
  background: none;
  border: none;
  color: white;
  cursor: pointer;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  margin-bottom: 50px;
}

#bouncy-btn .material-symbols-outlined {
  font-size: 2.5rem;
  transition: transform 0.4s;
}
</style>