<template>
  <Layout>
    <Content>
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
.error {
  color: #ed4014;
}

.layout-default {
  // min-height: 100vh;
}

.main-content {
  // height: calc(100vh - 60px);
  // padding: 18px;

  > div {
    background-color: white;
  }
}

.menu-top {
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 82px;
  background: #00C0E4;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 99999;
}

.logo-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  color: white;
  font-size: 18px;

  img {
    width: 24px;
    margin-right: 6px;
    display: inline-block;
  }
}

.nav-container {
  flex-grow: 1;
}

</style>
