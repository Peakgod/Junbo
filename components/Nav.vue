<template>
  <Layout class="layout-default">
    <Row>
        <Col span="4">.</Col>
        <Col span="16">
          <Menu class="menu-top" mode="horizontal" theme="dark">
            <Row>
              <Col span="7">
                <div class="menu-logo">
                  <img src="http://www.qhxywl.com/wp-content/themes/qhxywl/images/logo.png" alt="">
                  <span>
                    客户至上　用心服务
                    <br/>
                    资深网站建设服务商
                  </span>
                </div>
              </Col>
              <Col span="13">
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
              </Col>
              <Col span="4">
                <div class="menu-logo">
                  <Icon type="md-call" size="30" color="white"/>
                  <span class="menu-phone">
                    0971-8202846
                    <br/>
                    139 9701 2536
                  </span>
                </div>
              </Col>
            </Row>
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

.layout-default {
  background: #00C0E4;
  width: 100%;
  height: 82px;
  position: fixed;
  top: 0;
  left: 0;
  .menu-top {
    height: 82px;
    background: #00C0E4;
    width: 100%;
    .menu-logo {
      width: 100%;
      height: 82px;
      display: flex;
      align-items: center;
      justify-content: center;
      img {
        margin-right: 20px;
      }
      i {
        margin-right: 5px;
      }
      span {
        color: #fff;
        font-weight: 900;
        line-height: 1.8;
      }
      .menu-phone {
        font-size: 22px;
        color: #fff;
        font-weight: bold;
        line-height: 30px;
      }
    }
    .nav-container {
      width: 100%;
      height: 82px;
      display: flex;
      align-items: center;
      justify-content: center;
      .ivu-menu-item {
        padding: 0 14px;
      }
    }
  }
}
.ivu-menu-dark.ivu-menu-horizontal .ivu-menu-item {
  color: #fff;
} 
.ivu-menu-dark.ivu-menu-horizontal .ivu-menu-item-active,
.ivu-menu-dark.ivu-menu-horizontal .ivu-menu-submenu-active {
  color: rgb(255, 255, 255);
  border: 1px solid #fff;
  border-radius: 15px;
  line-height: 30px;
}
</style>
