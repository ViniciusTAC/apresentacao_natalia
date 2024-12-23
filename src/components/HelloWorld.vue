<template>
  <v-app>
    <v-container>
      <v-carousel
        cycle
        height="95vh"
        hide-delimiters
        show-arrows-on-hover
      >
        <v-carousel-item
          v-for="(image, index) in images"
          :key="index"
        >
          <v-img
            :src="image.src"
            :alt="image.alt"
            contain
            class="carousel-image"
          ></v-img>
          <div class="caption">
            <strong>{{ image.alt }}</strong>
          </div>
        </v-carousel-item>
      </v-carousel>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { src: require('@/assets/slide1.png'), alt: 'Slide 1' },
        { src: require('@/assets/slide2.png'), alt: 'Slide 2' },
        { src: require('@/assets/slide3.png'), alt: 'Slide 3' },
        { src: require('@/assets/slide4.png'), alt: 'Slide 4' },
        { src: require('@/assets/slide5.png'), alt: 'Slide 5' },
        { src: require('@/assets/slide6.png'), alt: 'Slide 6' },
        { src: require('@/assets/slide7.png'), alt: 'Slide 7' },
        { src: require('@/assets/slide8.png'), alt: 'Slide 8' },
      ],
    };
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}

.carousel-image {
  height: 90vh;
}

.caption {
  text-align: center;
  font-size: 18px;
  margin-top: 10px;
}
</style>
