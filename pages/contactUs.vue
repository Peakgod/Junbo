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
      <div class="secondContentText">
        <div class="secondContentTextLeft">
          <div class="secondContentTextLeftIcon">
            <ul class="iconContent">
              <li>ssssssss</li>
            </ul>
          </div>
        </div>
        <div class="secondContentTextright"></div>
      </div>

    </div>

  </div>
</template>
  
<script>
export default {
  data () {
    return {
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
      display: flex;
      justify-content: center;
      .secondContentText {
        display: flex;
        width: 80%;
        .secondContentTextLeft {
          width: 50%;
          height: 100%;
          background-color: rgb(219, 174, 240);
          .secondContentTextLeftIcon {
            margin: 5% 0;
            height: 80%;
            width: 50%;
            margin-left: 40%;
            background-color: #fff;
            padding-top: 80px;
            .iconContent {
              background-position: 0 0;
              width: 300px;
              li {
                background-image: url('../static/i_icon2.png');
                padding-left: 60px;
                font-size: 16px;
                margin-bottom: 20px;
                line-height: 35px;
              }
            }
          }
        }
        .secondContentTextright {
          width: 50%;
          height: 100%;
          background-color: rgb(185, 188, 221);
        }
      }
    }
  }

</style>