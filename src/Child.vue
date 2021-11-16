<template>
  <div>
    <a href="abc" target="_blank">
      <img src="./assets/carouse-item.png" />
      <div class="position-relative">
        <div class="banner-description">
          <span class="banner-title">
            <a v-bind:href="'#'">#</a>
            TITLE<br />
          </span>
          <span class="banner-alternative-text">
            <a v-bind:href="'#'">#</a>
            DESCRIPTION<br />
          </span>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: ["item"]
}
</script>

<style lang="stylus">
.banner-description
    background: black;
    position: absolute;
    z-index: 999;
    bottom: 0;
    padding: 5px 200px 5px 20px;
    max-height: 100px;
    text-align: left
    max-width: 640px
.banner-title
    color: white;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
.banner-alternative-text
    color: white;
    font-weight: 300;
    font-size: 16px;
    line-height: 24px;
    word-break: breakword

.position-relative
    position: relative !important
</style>
