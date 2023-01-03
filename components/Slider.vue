<template>
  <Flickity
    v-if="isMounted"
    ref="flickity"
    class="Slider"
    :options="flickityOptions"
    ><slot
  /></Flickity>
  <div v-else class="Slider Slider--placeholder">
    <slot />
  </div>
</template>

<script>
import imagesLoaded from 'imagesloaded'

export default {
  name: 'Slider',
  components: {
    Flickity: () => import('vue-flickity'),
  },
  props: {
    options: {
      type: Object,
      default: () => ({}),
    },
  },
  data() {
    return {
      isMounted: false,
    }
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
  mounted() {
    this.isMounted = true
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

<style lang="scss">
.Slider--placeholder > :not(:first-child) {
  display: none;
}
.Slider {
  margin-bottom: 1em;
  .flickity-prev-next-button {
    color: #2a659b;
    &:hover {
      color: #b5dff4;
    }
  }
}
</style>
