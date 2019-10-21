<template>
    <div id="NewsInformation">
        <div class="container">
            <div class="container text-center">
<!--                <h3>News</h3>-->
<!--                <p style="color:#b2b2b2"> News</p>-->
            </div>
            <div class="nav container text-center">
                <a href="#" class="active">Company News</a>
<!--                <a href="#">行业动态</a>-->
            </div>
            <ul class="news-container container-fuild">
                <li v-for="(item,index) in newsList" :key="index" class="wow fadeIn">
                    <div class="content">
                        <p>{{item.title}}</p>
                        <p>{{item.introduce}}</p>
                    </div>
                    <div class="time">
                        <p>{{item.date}}</p>
                        <span>{{item.year}}</span>
                    </div>
                    <div class="circle">
                        <img src="../assets/img/circle.png">
                        <i class="line center-block"></i>
                    </div>
                </li>
            </ul>
            <div class="contaianer-fuild text-center more">
                <i class="glyphicon glyphicon-th"></i>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'NewsInformation',
    data(){
        return{
            newsList:[
                {
                    id: '001',
                    title: 'Windows 10 May be back to ground-glass effects',
                    introduce: 'Some news shows that the update after Win10 is likely to bring back Aero Glass recently about Windows 10 "Project Neon" Project has received more attention, it is reported that the focus of the Project is to Win10 user UI a major renovation.',
                    date: '05-24',
                    year: '2018'
                },{
                    id: '002',
                    title: 'Microsoft has announced the Windows Vista life cycle is approaching',
                    introduce: 'According to Microsoft\'s life cycle diagram, Windows Vista will no longer be able to receive security updates from Microsoft when all support is discontinued on April 11, and various bugs that have not been fixed will be targeted by hackers',
                    date: '07-24',
                    year: '2018'
                },{
                    id: '003',
                    title: 'It took five years for apple to finally buy the iCloud.net domain name',
                    introduce: 'It is reported that iCloud.net is a domestic social networking site, providing one-stop content query, can view friends published the latest content. After apple bought the domain, the site will stop all services at the end of the month.',
                    date: '02-20',
                    year: '2019'
                },{
                    id: '004',
                    title: 'The 12th China software channel conference opened',
                    introduce: 'Beijing, Feb. 16, 2019 -- the 2017 China software ecology conference hosted by China software network will enter its 12th year. As always, the conference will bring a strong lineup of guests, highly professional, insightful and valuable content and interaction, as well as the most intense ecological docking and collision of ideas.',
                    date: '03-14',
                    year: '2019'
                }

            ]
        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    },
}
</script>
<style scoped>
.nav{
    margin: 20px 0;
}
.nav>a{
    display: inline-block;
    text-decoration: none;
    width: 120px;
    height: 45px;
    line-height: 45px;
    color: #333;
    border: 1px solid #333;
}
.nav>a.active{
    color: #1e73be;
    border-color: #1e73be;
}
.nav>a:hover{
    color: #1e73be;
    border-color: #1e73be;
}
.news-container{
    overflow: hidden;
    margin-bottom: 0;
}
.news-container>li{
    width: 55.6%;
    height: 120px;
    float: left;
    color: #333;
    text-align: right;
    border-left: 1px solid transparent;
    border-right: 1px solid transparent;
}
.news-container>li:hover{
    color: #1e73be;
    border: 1px solid #1e73be;
    cursor: pointer;
}
.news-container>li:nth-of-type(2n){
    float: right;
    text-align: left;
}
.news-container>li>.content{
    width: 60%;
    float: left;
    padding: 20px 0;
}
.news-container>li>.time{
    width: 20%;
    float: left;
    padding: 10px 0;
}
.news-container>li>.time>p{
    font-size: 30px;
    margin: 5px 0;
}
.news-container>li>.circle{
    width: 20%;
    height: 100%;
    float: left;
    position: relative;
}
.news-container>li>.circle>img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    width: 20px;
    height: 20px;
}
.news-container>li>.circle>i{
    display: block;
    width: 1px;
    height: 100%;
    background: #707070;
}
.news-container>li:nth-of-type(2n)>.content{
    float: right;
}
.news-container>li:nth-of-type(2n)>.time{
    float: right;
}
.news-container>li:nth-of-type(2n)>.circle{
    float: right;
}
.news-container>li:nth-of-type(1)>.circle>i{
    height: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
}
.more{
    font-size: 25px;
    color: #707070;
}
.more>i{
    cursor: pointer;
}
@media screen and (max-width: 767px){
    .news-container>li{
        width: 100%;
    }
    .news-container>li>.content{
        width: 70%;
        text-align: left;
        float: right;
    }
    .news-container>li>.time{
        width: 30%;
        text-align: left;
        float: right;
    }
    .news-container>li>.circle{
        display: none;
    }
}
</style>

