<template>
    <div class="photo-grid">
      <q-card v-for="photo in photos" :key="photo.id" class="my-card">
        <q-img :src="photo.src" :alt="photo.alt" />
      </q-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        photos: [
          { id: 1, src: 'https://somoskudasai.com/wp-content/uploads/2020/04/81ZNkhqRvVL.jpg', alt: 'Photo 1' },
          { id: 2, src: 'https://wallpapercave.com/wp/wc1715541.jpg', alt: 'Photo 2' },
          { id: 3, src: 'https://images2.alphacoders.com/100/thumb-1920-1001725.jpg', alt: 'Photo 3' },
          { id: 4, src: 'https://wallpapercave.com/wp/wp9801383.jpg', alt: 'Photo 4' },
          { id: 5, src: 'https://wallpaperaccess.com/full/5923449.jpg', alt: 'Photo 5' },
          { id: 6, src: 'https://wallpapercave.com/wp/wp2745298.jpg', alt: 'Photo 6' },
          { id: 7, src: 'https://getwallpapers.com/wallpaper/full/4/7/f/248620.jpg', alt: 'Photo 7' },
          { id: 8, src: 'https://getwallpapers.com/wallpaper/full/1/7/8/1463280-large-anime-hd-wallpaper-2560x1440-2560x1440.jpg', alt: 'Photo 8' },
          { id: 9, src: 'https://wallpaperaccess.com/full/1611633.jpg', alt: 'Photo 9' },
          { id: 10, src: 'https://wallpapercave.com/wp/Q423sdL.jpg', alt: 'Photo 10' },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .photo-grid {
    display:flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  
  .my-card {
    width: 150px;
  }
  </style>
  