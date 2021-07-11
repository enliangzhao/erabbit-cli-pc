<template>
  <div class="page-home">
    <div class="home-entry">
      <div class="container">
        <!-- 左侧分类 -->
        <HomeCategory />
        <home-banner></home-banner>
        <home-new ></home-new>
        <home-hot></home-hot>
        <home-brand></home-brand>
      </div>
    </div>
  </div>
</template>
<script>
import HomeBanner from './components/home-banner.vue'
import HomeCategory from './components/home-category'
import HomeNew from './components/home-new'
import HomeHot from './components/home-hot.vue'
import HomeBrand from './components/home-brand.vue'

export default {
  name: 'PageHome',
  components: { HomeCategory, HomeBanner, HomeNew, HomeHot, HomeBrand }
}
</script>
<style scoped lang="less">
</style>
