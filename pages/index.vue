<template>
  <div>
    <p>
      Solidan, is a higher education consulting company that delivers expert
      information technology and integration support provided by true Enrollment
      Management practitioners. We have over 60+ years of combined experience in
      admissions, financial aid, marketing, analytics, training, integration,
      and IT support. We have been in your shoes.
    </p>
    <Slider :options="sliderOptions">
      <img
        :srcset="require('~/assets/images/student.jpg').srcSet"
        alt="Medical student"
      />
      <img
        :srcset="
          require('~/assets/images/darya-tryfanava-d55fhArDES0-unsplash.jpg')
            .srcSet
        "
        alt="University building"
      />
      <img
        class="students"
        :srcset="
          require('~/assets/images/naassom-azevedo-Q_Sei-TqSlc-unsplash.jpg')
            .srcSet
        "
        alt="Group of students lounging"
      />
      <img
        :srcset="
          require('~/assets/images/pang-yuhao-_kd5cxwZOK4-unsplash.jpg').srcSet
        "
        alt="Graduates throwing their caps in the air"
      />
    </Slider>
    <p>
      We specialize in providing consulting for Technolution's Slate, PeopleSoft
      Campus Solutions, and system integrations. Our services provide both
      leadership and full implementation teams posed to augment resources.
      Solidan focuses on moving forward and achieving strategic and operational
      excellence for your academic institution. Our mission is to ensure your
      systems are seamless and working for you. With years of satisfied clients,
      we have established a continued relationship with the greater Higher
      Education Industry.
    </p>
  </div>
</template>

<script>
import Slider from '~/components/Slider.vue'

export default {
  name: 'Home',
  components: {
    Slider,
  },
  data() {
    return {
      sliderOptions: {
        adaptiveHeight: true,
        autoPlay: true,
        imagesLoaded: true,
        pageDots: false,
        wrapAround: true,
      },
    }
  },
}
</script>

<style lang="scss">
.students {
  aspect-ratio: 3/2;
  object-fit: cover;
  object-position: bottom center;
}
</style>
