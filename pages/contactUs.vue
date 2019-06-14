<template>
  <div class="content">
    <div class="contentFirst">
      <div class="firstContactText">
        <p>联系我们</p>
        <hr class="contactHr">
        <p class="contactPTow">5年西宁网站建设老品牌，已为100+集团企业及政府机构提供网站制作解决方案。</p>
      </div>
    </div>

    <div class="contentSecond">
      <div class="contactText">
        <h3>联系我们</h3>
        <h5>contact 8202846</h5>
      </div>
      <div class="secondContentText">
        <div class="secondContentTextLeft">
          <div class="secondContentTextLeftIcon">
            <div class="address">
              <p>
                青海省西宁市城东区昆仑东路299号9号楼1单元114室
              </p>
            </div>
            <div class="phone">
              <a href="#"> 139 9701 2536(业务咨询) </a>
              <a href="#"> 139 9701 2536(业务咨询) </a>
              <a href="#"> 139 9701 2536(业务咨询) </a>
            </div>
            <div class="mail">
              <a>
                344354835@qq.com
              </a>
            </div>
          </div>
        </div>

        <div class="secondContentTextright">
          <Form ref="formValidate" :model="formValidate" :rules="ruleValidate" :label-width="90">
            <Row>
              <Col span="11">
                <FormItem prop="name">
                  <Input v-model="formValidate.name" size="large" placeholder="姓名"></Input>
                </FormItem>
              </Col>

              <Col span="2" style="text-align: center">
                &nbsp;
              </Col>

              <Col span="11">
                <FormItem prop="phone">
                  <Input v-model="formValidate.phone" size="large" placeholder="联系方式"></Input>
                </FormItem>
              </Col>
            </Row>

            <FormItem prop="text">
              <Input v-model="formValidate.text" type="textarea" :autosize="{minRows: 5,maxRows: 5}" placeholder="请描述您的需求，如网站建设，微信公众号开发，微信小程序开发，网站改版，网站运营与维护，手机app开发，各类软件定制开发。"></Input>
            </FormItem>

            <FormItem>
              <Button class="formButton" type="primary" long @click="handleSubmit('formValidate')">提交</Button>
            </FormItem>
          </Form>
        </div>
      </div>

    </div>


    <div class="mapStyle">
      <baidu-map class="map" :center="{lng: 101.8037500000, lat: 36.5983200000}" :zoom="15" :scroll-wheel-zoom="true">
        <bm-marker :position="markerPoint" :dragging="true">
          <bm-info-window>我爱北京天安门</bm-info-window>
        </bm-marker>
      </baidu-map>
    </div>
  </div>
</template>
  
<script>
import BaiduMap  from 'vue-baidu-map/components/map/Map.vue'

export default {
  components: {
    BaiduMap
  },
  data () {
    return {
      markerPoint: '',

      formValidate: {
        name: '',
        phone: '',
        text: '',
      },

      ruleValidate: {
        name: [
          { required: true, message: '请填写', trigger: 'blur' }
        ],
        phone: [
          { required: true, message: '请填写', trigger: 'blur' },
        ],
        text: [
          { required: true, message: '请填写', trigger: 'blur' },
        ]
      }
    }
  },
  methods: {
    handleSubmit(name) {
      this.$refs[name].validate((valid) => {
        if (valid) {
            this.$Message.success('Success!');
        } else {
            this.$Message.error('Fail!');
        }
      })
    }
  }
}

    
</script>
<style scoped lang='less'>
  .content{
    .contentFirst {
      height: 269px;
      background-image: url(../static/lianxiwom.png);
      background-repeat: no-repeat;   //不重复
      background-size: 100% 100%;
      .firstContactText {
        margin-left: 330px;
        padding-top: 70px;
        font-size: 32px;
        color: white;
      }
      .contactHr {
        height: 2px;
        background-color: white;
        width: 50px;
        margin-top: 25px;
      }
      .contactPTow {
        font-size: 22px;
        margin-top: 30px;
      }
    }
    .contentSecond {
      z-index: -20;
      height: 428px;
      background-image: url('../static/联系--2.jpg');
      background-repeat: no-repeat;   //不重复
      background-size: 100% 100%;
      .contactText {
        padding-top: 50px;
        text-align: center;
        font-size: 30px;
        color: #002;
        margin-bottom: 10px;
        font-weight: 800;
      }
    }
    .secondContentText {
      display: flex;
        .secondContentTextLeft {
          width: 50%;
          height: 100%;
          .secondContentTextLeftIcon {
            margin: 3% 0;
            height: 80%;
            width: 50%;
            margin-left: 40%;
            .address {
              background-image: url('../static/i_icon1.png');
              background-repeat: no-repeat;   //不重复
              margin-left: 20px;
              height: 20%;
              margin-bottom: 25px;
              display: flex;
              align-items: center;
              p {
                margin-left: 50px;
                font-size: 16px;
                line-height: 30px;
                color: black;
              }
            }
            .phone {
              background-image: url('../static/i_icon3.png');
              background-repeat: no-repeat;   //不重复
              margin-left: 20px;
              height: 20%;
              margin-bottom: 40px;
              width: 300px;
              a {
                margin-left: 50px;
                font-size: 16px;
                line-height: 30px;
                color: black;
              }
            }
            .mail {
              background-image: url('../static/i_icon1.png');
              background-repeat: no-repeat;   //不重复
              margin-left: 20px;
              height: 20%;
              margin-bottom: 25px;
              display: flex;
              align-items: center;
              a {
                margin-left: 50px;
                font-size: 16px;
                line-height: 30px;
                color: black;
              }
            }
          }
        }
        .secondContentTextright {
          width: 30%;
          height: 100%;
          margin: 1% 0;
          .formButton {
            width: 100%;
            height: 40px;
            text-align: center;
            color: #fff;
            background-color: #00C0E4;
            border: 0;
            cursor: pointer;
            font-family: "微软雅黑","Microsoft Yahei";
            font-size: 16px;
          }
        }
    }
    .mapStyle {
      width: 100%;
      background-color: rgb(224, 224, 224);
      padding: 10px 5px 0 5px;
      .map {
        width: 100%;
        height: 500px;
      　.anchorBL {
          display: none;
        }
      }
    }
  }
</style>