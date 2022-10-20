<template>
  <SVGSprite />
  <div class="wrapper">
    <VueHeader />
    <main></main>
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view /> -->
    <VueFooter />
  </div>
</template>

<script>
import SVGSprite from "./components/SVGSprite.vue";
import VueHeader from "./components/VueHeader.vue";
import VueFooter from "./components/footer/VueFooter.vue";
export default {
  data() {
    return {};
  },
  components: { SVGSprite, VueHeader, VueFooter },
};
</script>

<style lang="scss">
@import "./sass/variables";
@import "./sass/mixins";
@import "./sass/functions";
@import "./sass/global/fonts";
@import "./sass/global/reboot";
@import "./sass/global/utils";
@import "./sass/global/container";
// Blocks
// ---------------------------------

@import "./sass/blocks/modal";
@import "./sass/blocks/btn";
@import "./sass/blocks/custom-input";
@import "./sass/blocks/custom-toggle";
@import "./sass/blocks/custom-select";
@import "./sass/blocks/link";
@import "./sass/blocks/title";
@import "./sass/blocks/text";
@import "./sass/blocks/data-accordion";
@import "./sass/blocks/btn-to-top";
@import "./sass/blocks/data-tabs";
@import "./sass/blocks/tabs";
@import "./sass/blocks/breadcrumbs";
@import "./sass/blocks/header";
@import "./sass/blocks/main-nav";
@import "./sass/blocks/burger";
@import "./sass/blocks/hero";
@import "./sass/blocks/hero-section";
@import "./sass/blocks/directions";
@import "./sass/blocks/techpark";
@import "./sass/blocks/about-company";
@import "./sass/blocks/history";
@import "./sass/blocks/numbers";
@import "./sass/blocks/principles";
@import "./sass/blocks/team";
@import "./sass/blocks/career";
@import "./sass/blocks/blog";
@import "./sass/blocks/contact-us";
@import "./sass/blocks/partners";
@import "./sass/blocks/tech";
@import "./sass/blocks/services";
@import "./sass/blocks/technic";
@import "./sass/blocks/projects";
@import "./sass/blocks/our-science";
@import "./sass/blocks/projects-page";
@import "./sass/blocks/catalog";
@import "./sass/blocks/project-hero";
@import "./sass/blocks/technologies";
@import "./sass/blocks/project-technic";
@import "./sass/blocks/video";
@import "./sass/blocks/gallery";
@import "./sass/blocks/similar-projects";
@import "./sass/blocks/our-history";
@import "./sass/blocks/our-vision";
@import "./sass/blocks/achievements";
@import "./sass/blocks/recycling";
@import "./sass/blocks/technic-and-methods";
@import "./sass/blocks/reviews";
@import "./sass/blocks/cooperation";
@import "./sass/blocks/we-need";
@import "./sass/blocks/work-with-us";
@import "./sass/blocks/vacancies";
@import "./sass/blocks/vacancy";
@import "./sass/blocks/vehicle-park";
@import "./sass/blocks/promo";
@import "./sass/blocks/blog-page";
@import "./sass/blocks/blog-article";
@import "./sass/blocks/rent-hero";
@import "./sass/blocks/rent-hero-desc";
@import "./sass/blocks/rent-technic";
@import "./sass/blocks/rent-selections";
@import "./sass/blocks/rent-about-us";
@import "./sass/blocks/catalog";
@import "./sass/blocks/catalog-filter";
@import "./sass/blocks/catalog-items";
@import "./sass/blocks/card";
@import "./sass/blocks/card-description";
@import "./sass/blocks/rent-card-characteristics";
@import "./sass/blocks/card-similar";
@import "./sass/blocks/vehicle-card";
@import "./sass/blocks/sale-goods-types";
@import "./sass/blocks/goods";
@import "./sass/blocks/delivery-calc";
@import "./sass/blocks/sale-selections";
@import "./sass/blocks/ecology";
@import "./sass/blocks/sale-about-us";
@import "./sass/blocks/road-build-hero";
@import "./sass/blocks/map";
@import "./sass/blocks/docs";
@import "./sass/blocks/contacts";
@import "./sass/blocks/directions-sup";
@import "./sass/blocks/topical";
@import "./sass/blocks/footer";

// ---------------------------------
</style>
