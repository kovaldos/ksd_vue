<template>
  <section class="section directions directions--main">
    <div class="container directions__container">
      <div class="directions__heading">
        <h2 class="title title--h2 directions__title">{{ main.title }}</h2>
        <h3 class="title title--h3 directions__subtitle">
          {{ main.subtitle }}
        </h3>
      </div>
      <div class="directions__cols">
        <div class="directions__col directions__col--01">
          <swiper
            class="swiper directions__text-slider"
            :watch-overflow="true"
            :auto-height="true"
            :modules="[Controller]"
            @swiper="setControlledSwiper"
            :enabled="swiperOptions.enabled"
          >
            <swiper-slide v-for="item in main.textItems" :key="item.id">
              <div class="directions__text-slider-item">
                <h4 class="title title--h4 directions__content-title">
                  {{ item.title }}
                </h4>
                <p class="text text--lg directions__text">
                  {{ item.text }}
                </p>
              </div>
            </swiper-slide>
          </swiper>
          <div class="directions__slider-nav">
            <div class="directions__slider-pag"></div>
            <div class="directions__slider-btns">
              <div
                class="swiper-button-next directions__slider-btn directions__slider-btn--next"
              >
                <svg width="30" height="30" aria-hidden="true">
                  <use xlink:href="#icon-chevron-right-black"></use>
                </svg>
              </div>
              <div
                class="swiper-button-prev directions__slider-btn directions__slider-btn--prev"
              >
                <svg width="30" height="30" aria-hidden="true">
                  <use xlink:href="#icon-chevron-left-black"></use>
                </svg>
              </div>
            </div>
          </div>
        </div>
        <div class="directions__col directions__col--02">
          <swiper
            class="swiper directions__slider"
            :modules="modules"
            :navigation="navigation"
            :pagination="pagination"
            :watch-overflow="true"
            :speed="1200"
            :effect="'coverflow'"
            :coverflow-effect="coverflow"
            :grab-cursor="true"
            :controller="{ control: controlledSwiper }"
          >
            <swiper-slide
              class="swiper-slide"
              v-for="item in main.items"
              :key="item.id"
            >
              <div class="directions__slider-item">
                <img
                  :src="require(`@/assets/img/${item.src}/${item.img}.jpg`)"
                  :srcset="
                    require(`@/assets/img/${item.src}/${item.img}.jpg`) + ' 2x'
                  "
                  :alt="item.alt"
                />
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from "vue";
import { Navigation, Pagination, Controller, EffectCoverflow } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";

export default {
  data() {
    return {
      main: {
        title: "Направления",
        subtitle: "100% безотходное производство",
        textItems: [
          {
            id: "id-directions-text-item-1",
            title: "Демонтаж зданий и сооружений",
            text: "Полный комплекс услуг по демонтажу зданий и сооружений: от разработки исходно-разрешительной документации до вывоза строительных отходов.",
          },
          {
            id: "id-directions-text-item-2",
            title: "Демонтаж зданий и сооружений 2",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum eos non, voluptates provident fugiat enim illum repellendus quidem vel soluta in accusantium vero sequi quaerat sed officia, voluptate fugit voluptatum quae, excepturi necessitatibus facilis doloribus expedita labore. Recusandae iure voluptatem perferendis inventore, eos consectetur, quos quo doloribus nisi deleniti laborum.",
          },
          {
            id: "id-directions-text-item-3",
            title: "Демонтаж зданий и сооружений 3",
            text: "Полный комплекс услуг по демонтажу зданий и сооружений: от разработки исходно-разрешительной документации до вывоза строительных отходов.",
          },
          {
            id: "id-directions-text-item-4",
            title: "Демонтаж зданий и сооружений 4",
            text: "Полный комплекс услуг по демонтажу зданий и сооружений: от разработки исходно-разрешительной документации до вывоза строительных отходов.",
          },
          {
            id: "id-directions-text-item-5",
            title: "Демонтаж зданий и сооружений 5",
            text: "Полный комплекс услуг по демонтажу зданий и сооружений: от разработки исходно-разрешительной документации до вывоза строительных отходов.",
          },
        ],
        items: [
          {
            id: "id-directions-img-slide-1",
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            id: "id-directions-img-slide-2",
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            id: "id-directions-img-slide-3",
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            id: "id-directions-img-slide-4",
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            id: "id-directions-img-slide-5",
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
        ],
      },
      recycling: {
        title: "Технопарк",
        subtitle:
          "Высокотехнологичная площадка по переработке строительных отходов",
        contentTitle: "",
        textItems: [
          {
            title: "Переработка строительных отходов",
            text: "В 2022 году в Московской области открыт завод по переработке строительных отходов.",
            text1:
              "Собственный комплекс по производству материалов из вторсырья дает возможность работать с объемом свыше 5 тыс. тонн строительных отходов ежедневно.",
          },
          {
            title: "Переработка строительных отходов 2",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam pariatur rerum tenetur harum sapiente porro autem perspiciatis impedit quo. Maxime?",
            text1:
              "Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam pariatur rerum tenetur harum sapiente porro autem perspiciatis impedit quo. Maxime?",
          },
          {
            title: "Переработка строительных отходов 3",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam pariatur rerum tenetur harum sapiente porro autem perspiciatis impedit quo. Maxime?",
            text1:
              "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officiis eum maxime rem explicabo ad a repellat necessitatibus, consequatur eveniet deserunt quo tenetur, accusamus porro quis iusto nostrum, ipsum eius similique!",
          },
          {
            title: "Переработка строительных отходов 4",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores alias iste delectus itaque possimus maxime pariatur recusandae, velit est ex cumque maiores. Illo optio ipsam eos consequatur ab molestias officiis repellendus, temporibus, velit magni, omnis aperiam esse nulla dolore ex!",
            text1:
              "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores alias iste delectus itaque possimus maxime pariatur recusandae, velit est ex cumque maiores. Illo optio ipsam eos consequatur ab molestias officiis repellendus, temporibus, velit magni, omnis aperiam esse nulla dolore ex!",
          },
          {
            title: "Переработка строительных отходов 5",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores alias iste delectus itaque possimus maxime pariatur recusandae, velit est ex cumque maiores. Illo optio ipsam eos consequatur ab molestias officiis repellendus, temporibus, velit magni, omnis aperiam esse nulla dolore ex!",
            text1:
              "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequuntur numquam tenetur unde doloremque? Quisquam ducimus vitae totam. Optio repudiandae eaque fuga unde illo neque suscipit minus reiciendis quisquam? Rem accusamus doloribus nemo sed dignissimos veniam eum, magni aperiam obcaecati nam, minima dolorem quibusdam sapiente quis explicabo qui voluptatibus. Doloremque, fugiat.",
          },
        ],
        items: [
          {
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
          {
            src: "slides",
            img: "directions-img-1",
            alt: "экскаватор-разрушитель",
          },
        ],
        btn: {
          text: "Получить КП",
        },
      },
      modules: [Pagination, Navigation, Controller, EffectCoverflow],
      navigation: {
        nextEl: ".directions__slider-btn--next",
        prevEl: ".directions__slider-btn--prev",
      },
      pagination: {
        el: ".directions__slider-pag",
        type: "fraction",
      },
      coverflow: {
        rotate: -2,
        stretch: -500,
        depth: 215,
        modifier: -1,
        slideShadows: false,
      },
      swiperOptions: {
        enabled: false,
      },
    };
  },
  components: { Swiper, SwiperSlide },
  setup() {
    const controlledSwiper = ref(null);
    const setControlledSwiper = (swiper) => {
      controlledSwiper.value = swiper;
    };
    return {
      Controller,
      controlledSwiper,
      setControlledSwiper,
    };
  },
};
</script>

<style></style>
