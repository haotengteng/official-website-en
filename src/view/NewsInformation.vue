<template>
    <div id="NewsInformation">
        <div class="container">
            <div class="container text-center">
                <h3>新闻动态</h3>
                <p style="color:#b2b2b2">Company News</p>
            </div>
            <div class="nav container text-center">
                <a href="#" class="active">公司新闻</a>
                <a href="#">行业动态</a>
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
                    title: 'Windows 10或将重新请回毛玻璃特效',
                    introduce: '有消息显示，Win10之后的更新有可能将重新请回Aero Glass最近关于Windows 10的“Project Neon”计划项目受到了更多的关心，据悉该项目的重点内容是对Win10的用户UI进行一次大幅度改造。',
                    date: '05-24',
                    year: '2018'
                },{
                    id: '002',
                    title: '微软通告Windows Vista生命周期将至',
                    introduce: '根据微软的生命周期图，Windows Vista将于今年4月11日停止所有支持，届时该系统将不再能够接收到来自微软的安全更新，尚未修复的各种漏洞也将会成为黑客攻击的目标',
                    date: '07-24',
                    year: '2018'
                },{
                    id: '003',
                    title: '耗时五年 苹果终于购入iCloud.net域名',
                    introduce: '据悉，iCloud.net是一家国内的社交网站，提供一站式内容查询，可以查看朋友发布的最新内容。而在苹果收购该域名之后，该网站将在月底停止所有服务。',
                    date: '02-20',
                    year: '2019'
                },{
                    id: '004',
                    title: '第十二届中国软件渠道大会全面开启',
                    introduce: '北京2019年2月16日电 /美通社/ -- 由中国软件网主办的2017中国软件生态大会将步入第十二个年头，此次大会一如既往，将带来强大的嘉宾阵容、极具专业、洞察与价值的内容及互动以及最激烈的生态对接与思想碰撞。',
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

