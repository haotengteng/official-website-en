<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">ABOUT US</div>

        <div class="container">
            <div class="row CompanyIntroduction-container">
<!--              <div class="font-banner container-fuild text-center">公司介绍</div>-->
              <div class="container text-center">
                <h3>Company Introduction</h3>
<!--                <p style="color:#b2b2b2">Company Introduction</p>-->
              </div>
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>Zhongsheng software technology co. LTD</h3>
                    <p class=".text-justify">Zhongsheng software technology co., LTD., is a high-tech creativity as the core technology services company, gathered a number of software development and interface design has a unique creative talents, currently has 35 software designers and dedicated to provide software development for the enterprises at home and abroad, the website construction, web design, IT outsourcing, mobile application development, Internet marketing solutions.
                     </p>

                    <p class=".text-justify"> Our clients include group listed company, involved in the hotel, the IT technology, education, clothing, trade, foreign trade, fashion, biological, industrial, manufacturing and many other industries, and establish a good reputation, has accumulated rich experience and successful cases. We provide authoritative professional Internet brand planning, and implementation of high standards of design, to create a real brand site, to create maximum value for the Internet brand in the field of interactive marketing and make unremitting efforts!At present, we focus on developing overseas markets and provide software outsourcing services for developed countries such as Europe, America and Hong Kong</p>
                </div>
              </div>

<!--          <div class="font-banner container-fuild text-center">团队介绍</div>-->
          <div class="container text-center">
            <h3>Introduction To Core Team Members</h3>
<!--            <p style="color:#b2b2b2">Introduction To Core Team Members</p>-->
          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">Kevin</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">Technical director</p>
              <p class=".text-justify">Engaged in software development for many years, experienced, was in control group, the financial ministry of science and technology the backend development team leader, familiar with finance software development, good at Java and the surrounding technology, have a deep research on elasticSearch, deeply understand the mysql database storage and transaction mechanism, good at tasks for large scale project split and controls the whole project schedule.</p>
              <p class=".text-justify">I have developed large-scale Internet financial system, enterprise CRM,oa system, mall and communication software. Participated in the design of internal distributed framework development, and helped multiple enterprise back-end systems to realize the system upgrade from single package project to distributed project.</p>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
              <img class="img-responsive center-block photo-size" src="@/assets/img/photo_nan.jpg">
            </div>

          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">Davin</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">The development team leader</p>
              <p class=".text-justify">Graduated from China university of geosciences, served as the leader of netease corola server development, familiar with software development in the field of e-commerce, rich experience in high concurrency system design, in-depth understanding of rabbitMq and other messaging middleware, good at system design of various complex businesses, and experienced in dismantling complex system tasks</p><p class=".text-justify">Familiar with all kinds of cutting-edge technology in the industry, always keep the pursuit of new technology, give full play to the performance improvement of the system by all kinds of new technology</p>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
              <img class="img-responsive center-block photo-size" src="@/assets/img/photo_nan_2.png">
            </div>

          </div>
          <div class="row CompanyIntroduction-container">
            <div class="col-xs-12 col-sm-12 col-md-6">
              <h3 style="display: inline-block">Lily</h3> &nbsp;  <p style="color:#b2b2b2;display: inline-block">Large front end leader</p>
              <p class=".text-justify">Served as the front-end project manager of qunar.com, familiar with project requirements, good at streamlining complex business, with high business skills and skillful communication skills, able to help the team quickly enter the development stage from the beginning of the project</p>
              <p class=".text-justify">Good at the website layout design, stand in the user's point of view of the website interaction for in-depth improvement, the pursuit of the website usability and aesthetic acme</p>
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

