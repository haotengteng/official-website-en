<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>

        <div class="container">
            <div class="row CompanyIntroduction-container">
<!--              <div class="font-banner container-fuild text-center">公司介绍</div>-->
              <div class="container text-center">
                <h3>公司介绍</h3>
                <p style="color:#b2b2b2">Company Introduction</p>
              </div>
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>中盛软件技术有限公司</h3>
                    <p class=".text-justify">中盛软件技术有限公司, 是一家以高科技创意为核心的技术服务公司, 聚集了众多对软件开发和界面设计有独特创意的高端人才, 致力于为企业提供软件开发, 网站建设, 网页设计, IT外包, 手机应用开发, 互联网营销等解决方案。</p>
                    <p class=".text-justify">我们的客户包括集团上市公司, 酒店, IT科技, 教育, 服装, 贸易, 外贸, 时尚, 生物, 工业, 制造等众多行业, 并树立了良好的口碑, 积累了丰富的经验和成功案例. 我们提供权威专业的互联网品牌策划, 并实施高标准的设计方案, 创造真正意义上的品牌网站, 为互联网品牌在互动行销领域创造最大价值而不懈努力!</p>
                </div>
              </div>

<!--          <div class="font-banner container-fuild text-center">团队介绍</div>-->
          <div class="container text-center">
            <h3>团队核心人员介绍</h3>
            <p style="color:#b2b2b2">Introduction To Core Team Members</p>
          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">郝腾腾</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">技术总监</p>
              <p class=".text-justify">从事多年软件开发，经验丰富，曾担任泰然集团金融科技部后端开发组组长，熟悉金融领域的软件开发，擅长Java及其周边技术，对elasticSearch有深入研究，深入了解mysql数据库存储及其事务机制，擅长对大型项目的任务拆分和项目进度的整体把控。</p>
              <p class=".text-justify">曾开发过大型互联网金融系统，企业crm,oa系统，商城类和通信类软件。参与设计过企业内部分布式框架的开发，帮助多个企业后端系统实现由单包项目到分布式项目的系统升级。</p>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
              <img class="img-responsive center-block photo-size" src="@/assets/img/photo_nan.jpg">
            </div>

          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">徐进言</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">开发组长</p>
              <p class=".text-justify">毕业于中国地质大学，曾担任网易考拉服务器开发组长，熟悉电商领域的软件开发，对高并发的系统设计有丰富的经验，深入了解rabbitMq等消息中间件，擅长各种复杂业务的系统设计，对复杂系统的任务拆解经验丰富</p><p class=".text-justify">熟悉各种业界前沿技术，时刻保持对新技术的追求，充分发挥各种新技术对系统的性能提升</p>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
              <img class="img-responsive center-block photo-size" src="@/assets/img/photo_nan_2.png">
            </div>

          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">胡艳</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">大前端组长</p>
              <p class=".text-justify">曾担任去哪儿网大前端项目经理，熟悉项目需求梳理，擅长将复杂业务流程化，业务技能高，沟通技巧熟练，能帮助团队从项目开始阶段迅速进入开发；</p>
              <p class=".text-justify">擅长对网站的页面布局设计，站在用户的角度对网站的交互进行深入的改进，追求网站易用程度和美观的极致</p>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
              <img class="img-responsive center-block photo-size" src="@/assets/img/photo_nv4.jpeg">
            </div>

          </div>

            </div>

    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{

        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
 h3{
   color: #000000;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 50px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
.photo-size{
  width: 250px;
  height: 300px;
  margin-right: 100px;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

