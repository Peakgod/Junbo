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
          >
            <MenuItem
              :name="item.to"
            >
              {{item.title}}
            </MenuItem>
          </div>
        </no-ssr>
      </div>
    </Menu>

    <!-- <Footer>
      <Row type="flex" justify="center">
        <Col>2011-2018 © 西宁君博科技有限公司 版权所有</Col>
      </Row>
    </Footer> -->
  </Layout>
</template>

<script>

import routeTopConfig from '@/assets/config/router.top.config'

export default {
  data () {
    return {
      routeTopConfig,
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
