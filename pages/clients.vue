<template>
  <div class="clients-grid">
    <div
      v-for="image in clientImages"
      :key="image.name"
      class="clients-grid-item"
    >
      <img
        :src="getImageSrc(image.logo)"
        :alt="image.name"
        class="clients-grid-image"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Clients',
  data() {
    return {
      clientImages: [
        {
          name: 'Rochester Institute of Technology',
          logo: 'rit-logo.png',
        },
        {
          name: 'Bellevue University',
          logo: 'bellevue-logo.png',
        },
        {
          name: 'University of Connecticut',
          logo: 'university-connecticut.png',
        },
        {
          name: 'Loyola University Chicago',
          logo: 'loyola-university-chicago.png',
        },
        {
          name: 'City Colleges of Chicago',
          logo: 'logo_coe_vertical.png',
        },
        
        {
          name: 'UMASS',
          logo: 'UMASS-logo-NEW.jpg',
        },
      ],
    }
  },
  methods: {
    getImageSrc(filename) {
      return require(`~/assets/images/clients/${filename}`)
    },
  },
}
</script>

<style>
.clients-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.clients-grid-item {
  width: 33.333%;
}
.clients-grid-image {
  padding: 10%;
}
</style>
