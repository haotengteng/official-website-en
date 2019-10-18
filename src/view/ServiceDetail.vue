<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">相关服务</div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
            <p>特色服务</p>
            <li
              :class="item.id==id?'active':''"
              v-for="(item,index) in serviceNavList"
              :key="index"
            >
              <a :href="'#'+item.id">{{item.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div class="content-block" v-for="(item,index) in serviceContentList" :key="index">
            <h2 :id="item.id">
              {{item.title}}
              <small>/ {{item.eng_title}}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "软件定制开发"
        },
        // {
        //   id: "section-2",
        //   title: "IT外包服务"
        // },
        {
          id: "section-3",
          title: "网上商城建设"
        },
        {
          id: "section-4",
          title: "系统优化"
        }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "软件定制开发",
          eng_title: "Customize App",
          content:
            "<h3>后台系统 & 生产系统</h3><p>管理各种业务数据，权限与功能控制，了解生产进度状态，ERP、OA、CRM、MES系统\n" +
              "企业内部管理系统B/S架构、Web网页版系统、C/S架构客户端软件、HTML5+CSS3响应式布局、MySQL+Java架构</p>" +
              "<h3>安卓APP & 苹果APP</h3><p>安卓Android、苹果iOS两大平台，以及可针对pad和触摸屏开发。安卓Android APP\n" +
              "苹果iOS APP原生代码 & H5方式开发、电商类APP、社交类APP、内部管理、设备管理APP</p>"
        }
        // ,
        // {
        //   id: "section-2",
        //   title: "IT外包服务",
        //   eng_title: "Outsourcing",
        //   content:
        //     "<h3>整体IT外包</h3><p>选择整体外包服务，从此免去招聘、培训和管理专职IT技术人员的烦恼，我们负责您公司IT系统的运维、规划和采购等工作，为您提供全方位一站式的IT技术服务。\n" +
        //       "配套专职现场技术人员、配套专职IT顾问、配套专职客服专员、配套定制服务报告、加强病毒防范</p>"
        // }
        ,
        {
          id: "section-3",
          title: "网上商城建设",
          eng_title: "eCommerce Site",
          content:
            "<h3>零售版</h3><p>1.快速搭建B2C零售商城，快速铺货；2.多款吸粉利器，持续为店铺引流促销；</p>" +
              "<h3>分销版</h3><p>1.裂变分销，以客推客，打造超强分销大军；2.开启分销店中店，分销商也有自己的店铺；3.多维度佣金激励政策，刺激人人分享卖货；</p>"+
            "<h3>全能版</h3><p>1.独立供应商管理模块，解决上游货源烦恼；2.代理商独立后台，打通线下代理渠道；3.标准API接口开放，商城发展可拓展度更高；</p>"
        },
        {
          id: "section-4",
          title: "系统优化",
          eng_title: "system optimization",
          content:
            "<h3>系统调优</h3><p>为您解决当前系统存在的疑难问题，突破性能瓶颈，助力高效生产</p>"
        }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}
ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}
ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}
ul.nav-tabs li:first-child {
  border-top: none;
}
ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}
ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}
ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}
ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}
ul.nav-tabs.affix {
  top: 30px;
}
.content-block {
  margin: 50px 0;
}
.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
