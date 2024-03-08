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
}
.img-container {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.img-container img {
  max-width: 100%;
  max-height: 100%;
}
</style>
