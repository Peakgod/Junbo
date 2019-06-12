<template>
  <Layout class="layout-default">
    <Row>
        <Col span="4">.</Col>
        <Col span="16">
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
                    :key="item.name"
                    :to="item.to"
                    :name="item.to"
                  >
                    {{item.title}}
                  </MenuItem>
                </div>
              </no-ssr>
            </div>
          </Menu>
        </Col>
        <Col span="4">.</Col>
    </Row>
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
  background: #00C0E4;
  width: 100%;
}

.main-content {
  // height: calc(100vh - 60px);
  // padding: 18px;
  overflow: scroll;

  > div {
    padding: 18px;
    // background-color: white;
  }
}

.menu-top {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 82px;
  background: #00C0E4;
  // position: fixed;
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
