<template>
  <div class="home">
    <div class="img-container">
      <img ref="imgref" />
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue"
import imgUrl from "@/assets/img/2022.jpg"

const imgref = ref(null)

onMounted(() => {
  imgref.value.src = imgUrl
})
</script>

<style scoped>
.home {
  width: 100%;
  height: 100%;
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-direction: column;
  z-index: 10;
}
.img-container {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  overflow: hidden;
}
.img-container img {
  width: 100%;
}
</style>
