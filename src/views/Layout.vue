<template>
  <app-topnav></app-topnav>
  <app-header></app-header>
  <app-header-sticky></app-header-sticky>
  <div class="app-body">
    <!-- 二级路由 -->
    <router-view></router-view>
  </div>
  <app-footer></app-footer>
</template>

<script>
import AppTopnav from '@/components/app-topnav'
import AppHeader from '@/components/app-header'
import AppFooter from '@/components/app-footer'
import AppHeaderSticky from '@/components/app-header-sticky'
import { useStore } from 'vuex'
export default {
  name: 'xtx-layout',
  components: { AppTopnav, AppHeader, AppFooter, AppHeaderSticky },
  setup () {
    const store = useStore()
    store.dispatch('category/getList')
  }
}
</script>

<style scoped lang='less'>
.app-body{
  min-height: 600px;
}
</style>
