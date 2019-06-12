<template>
  <Layout class="layout-default">
    <Menu class="menu-top" mode="horizontal">
      <div class="logo-container">
        <!-- <img src="@/assets/images/logo.png" alt=""> -->
        <span>智能外呼中台系统</span>
      </div>

      <div class="nav-container">
        <no-ssr>
          <div
            v-for="(item, i) in routeTopConfig"
            :key=i
          >
            <MenuItem
              :name="item.to"
              :to="item.to"
            >
              {{item.title}}
            </MenuItem>
          </div>
        </no-ssr>
      </div>
    </Menu>

    <Footer />
  </Layout>
</template>

<script>

import routeTopConfig from '@/assets/config/router.top.config'
import Footer from '@/components/Footer'

export default {
  data () {
    return {
      routeTopConfig,
      Footer
    }
  },
  methods: {
  },
  mounted () {
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
  overflow: scroll;

  > div {
    padding: 18px;
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
