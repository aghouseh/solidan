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
          name: 'University of Southern Mississippi',
          logo: 'usm.jpg',
        },
        {
          name: 'UMASS',
          logo: 'UMASS-logo-NEW.jpg',
        },
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
          name: 'Benedictine University',
          logo: 'ben.png',
        },
        {
          name: 'Pennsylvania College of Art & Design',
          logo: 'pcad-logo.png',
        },
        {
          name: 'University of St. Thomas',
          logo: 'Primary Academic Mark-UST-logo-RED Vertical-JPG.jpg',
        },
        {
          name: 'RMIT University of Vietnam',
          logo: 'rmitVietnam.png',
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

<style lang="scss">
.clients-grid {
  @media (min-width: 640px) {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    align-items: center;
    gap: 2em;
  }
  margin-bottom: 3em;
}
.clients-grid-item {
  text-align: center;
  aspect-ratio: 3/2;
  display: flex;
  flex-direction: column;
  justify-content: center;
  @media (max-width: 639px) {
    margin-block-end: 2em;
  }
}
.clients-grid-image {
  place-self: center;
}
</style>
