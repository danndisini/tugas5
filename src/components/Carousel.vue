<template>
  <q-carousel
    v-model="slide"
    animated
    infinite
    swipeable
    autoplay
    autoplay-interval="3000"
  >
    <q-carousel-slide v-for="img in images" :name="img.name" :key="img.name">
      <img :src="img.src" class="carousel-image" />
    </q-carousel-slide>

    <q-carousel-control position="bottom-right">
      <q-btn round flat icon="keyboard_arrow_left" @click="prev" />
      <q-btn round flat icon="keyboard_arrow_right" @click="next" />
    </q-carousel-control>
  </q-carousel>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Carousel',
  setup() {
    const slide = ref(0)
    const images = [
      { name: '1', src: 'https://somoskudasai.com/wp-content/uploads/2020/04/81ZNkhqRvVL.jpg' },
      { name: '2', src: 'https://wallpapercave.com/wp/wc1715541.jpg' },
      { name: '3', src: 'https://images2.alphacoders.com/100/thumb-1920-1001725.jpg' },
      { name: '4', src: 'https://wallpapercave.com/wp/wp9801383.jpg' },
      { name: '5', src: 'https://wallpaperaccess.com/full/5923449.jpg' }
    ]

    const next = () => {
      slide.value = (slide.value + 1) % images.length
    }

    const prev = () => {
      slide.value = (slide.value - 1 + images.length) % images.length
    }

    return {
      slide,
      images,
      next,
      prev
    }
  }
}
</script>

<style scoped>
.carousel-image {
  width: 100%;
  height: auto;
}
</style>
