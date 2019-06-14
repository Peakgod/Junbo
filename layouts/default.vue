<template>
  <Layout>
    <Content class="main-nav">
      <Nav/>
    </Content>

    <Layout class="main-content">
      <nuxt />
    </Layout>

    <Footer />
  </Layout>
</template>

<script>

import routeTopConfig from '@/assets/config/router.top.config'
import Nav from '~/components/Nav'
// import Footer from '~/components/Footer.vue'

export default {
  components: {
    Nav
    // Footer
  },
  data () {
    return {
      routeTopConfig
    }
  },
  methods: {
    
  },
  mounted () {
    console.log(routeTopConfig);
  }
}
</script>

<style scoped lang="scss">
.main-nav {
  position: fixed;
  top: 0;
  z-index: 9999;
}

</style>
