<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          Free Welpap
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <q-list>
        <q-item clickable v-ripple @click="showPhotoGrid">
          <q-item-section>
            <q-item-label>Alll</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
      <div v-if="showingPhotoGrid">
        <PhotoGrid />
      </div>
      <div v-else>
        Hello selamat menikmati Walpaper grratis &#128512
        <Carousel />
      </div>
    </q-page-container>

    <Footer />
  </q-layout>
</template>

<script>
import { ref } from 'vue'
// Import the Footer component
import Footer from './components/Footer.vue'
// Import the Carousel component
import Carousel from './components/Carousel.vue'
import Card from './components/Card.vue'
import PhotoGrid from './components/PhotoGrid.vue'

export default {
  components: {
    Footer,
    Carousel,
    Card,
    PhotoGrid
  },
  setup () {
    const leftDrawerOpen = ref(false)
    const showingPhotoGrid = ref(false)

    return {
      leftDrawerOpen,
      showingPhotoGrid,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },
      showPhotoGrid () {
        showingPhotoGrid.value = true
      }
    }
  }
}
</script>
