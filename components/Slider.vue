<template>
  <client-only>
    <Flickity ref="flickity" :options="flickityOptions"><slot /></Flickity>
    <template #placeholder> Loading... </template>
  </client-only>
</template>

<script>
import imagesLoaded from 'imagesloaded'
import Flickity from 'vue-flickity'

export default {
  name: 'Slider',
  components: {
    Flickity,
  },
  props: {
    options: {
      type: Object,
      default: () => ({}),
    },
  },
  computed: {
    flickityOptions() {
      return {
        ...this.options,
        on: {
          ...(this.options.on || {}),
          ready: () => imagesLoaded(this.$refs.flickity.$el, this.loadComplete),
        },
      }
    },
  },
  methods: {
    loadComplete() {
      if (this.$refs.flickity) {
        this.$refs.flickity.reloadCells()
      }
    },
  },
}
</script>

<style lang="scss" scoped>
.flickity-enabled {
  margin-bottom: 1em;
  .button {
    color: #b5dff4;
  }
}
</style>
