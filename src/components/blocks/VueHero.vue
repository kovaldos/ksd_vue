<template>
  <section class="hero">
    <swiper
      class="swiper hero__slider"
      :modules="modules"
      :pagination="pagination"
      :watch-overflow="true"
      :loop="true"
      :speed="800"
      :effect="'fade'"
      :autoplay="autoplay"
    >
      <swiper-slide class="swiper-slide" v-for="item in items" :key="item.id">
        <router-link class="hero__slider-item" :to="item.href">
          <div class="hero__bg">
            <img
              :src="require(`@/assets/img/slides/${item.img}.jpg`)"
              :srcset="
                require(`@/assets/img/slides/${item.img}@2x.jpg`) + ' 2x'
              "
              :alt="item.alt"
            />
          </div>
          <div class="container hero__container">
            <div class="hero__heading">
              <h1 class="title title--h1 hero__title">
                {{ item.title
                }}<span class="hero__subtitle">{{ item.subtitle }}</span>
              </h1>
            </div>
          </div></router-link
        >
      </swiper-slide>
      <div class="hero__slider-pag"></div>
    </swiper>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, EffectFade, Autoplay } from "swiper";

export default {
  data() {
    return {
      items: [
        {
          id: "id-hero-slide-1",
          href: "demolition",
          title: "Quis scelerisque suspendisse risus arcu.",
          subtitle:
            "Consectetur nec tristique massa est nibh magna ac duis justo. Fermentum amet amet vitae sagittis congue nisi erat lectus.",
          img: "hero-bg-img-1",
          alt: "slide-img-1",
        },
        {
          id: "id-hero-slide-2",
          href: "demolition",
          title: "Lorem ipsum dolor sit.",
          subtitle:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam, earum!",
          img: "hero-bg-img-2",
          alt: "slide-img-2",
        },
        {
          id: "id-hero-slide-3",
          href: "roads",
          title: "Lorem ipsum dolor sit amet consectetur.",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          img: "hero-bg-img-3",
          alt: "slide-img-3",
        },
        {
          id: "id-hero-slide-4",
          href: "recycling",
          title: "Lorem ipsum dolor sit amet consectetur.",
          subtitle:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquam.",
          img: "hero-bg-img-4",
          alt: "slide-img-4",
        },
      ],
      autoplay: {
        disableOnInteraction: false,
        pauseOnMouseEnter: true,
      },
      pagination: {
        clickable: true,
        el: ".hero__slider-pag",
        type: "bullets",
        renderBullet(index, className) {
          console.log(index, className);
          return `
          <span class=${className}>
            <svg class="progress-ring" width="34" height="34">
              <circle class="progress-ring__circle" stroke="white" stroke-width="2" cx="17" cy="17" r="16" fill="currentColor"></circle>
            </svg>
          </span>
        `;
        },
      },
      modules: [Pagination, EffectFade, Autoplay],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<style></style>
