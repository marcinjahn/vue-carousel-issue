<template>
  <div id="app">
    <div class="banner-container">
      <div>
        <VueSlickCarousel v-bind="settings">
          <div v-for="item in items" :key="item.id">
            
            <!-- ALTERNATIVE 1 (WORKS) -->
            <div>
              <a href="abc" target="_blank">
                <img id="picture1" src="./assets/carouse-item.png" />
                <div class="position-relative">
                  <div class="banner-description">
                    <span class="banner-title">
                      <a v-bind:href="'#'" class="header-anchor">#</a>
                      TITLE<br />
                    </span>
                    <span class="banner-alternative-text">
                      <a v-bind:href="'#'" class="header-anchor">#</a>
                      DESCRIPTION<br />
                    </span>
                  </div>
                </div>
              </a>
            </div>

            <!-- ALTERNATIVE 2 (DOESN'T WORK) -->
            <!-- <Child :item="item"/> -->

          </div>
        </VueSlickCarousel>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
import Child from "./Child.vue";

export default {
  name: "App",
  components: { VueSlickCarousel, Child },
  data() {
    return {
      items: [
        {
          id: 1,
        },
        {
          id: 2,
        },
        {
          id: 3,
        },
      ],
      settings: {
      },
    };
  },
};
</script>

<style lang="stylus">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.banner-container
    text-align center
    margin auto
    width 100%

.banner-description
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0.3) , transparent);
    position: absolute;
    z-index: 999;
    bottom: 0;
    padding: 5px 200px 5px 20px;
    max-height: 100px;
    text-align: left
    max-width: 640px
.banner-title
    color: white
    font-weight: 500
    font-size: 16px;
    line-height: 24px;
.banner-alternative-text
    color: white
    font-weight: 300
    font-size: 16px;
    line-height: 24px;
    word-break: breakword

.carousel
    clear right

.position-relative
    position: relative !important
.slick-prev:before,
.slick-next:before {
  font-family: 'slick';
  font-size: 20px;
  line-height: 1;
  opacity: 0.75;
  color: black !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.banner-container{
    max-width: 1260px;
}
</style>
