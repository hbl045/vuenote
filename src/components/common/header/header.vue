<template>
    <!-- 头部导航 -->
    <div id="head" class="clearf">
      <!-- 左边导航 -->
      <div class="header-left">
          <ul>
            <li class="clearf"><a href="#">小米商城</a></li>
            <li class="clearf"><a href="#">MIUI</a></li>
            <li class="clearf"><a href="#">IoT</a></li>
            <li class="clearf"><a href="#">云服务</a></li>
            <li class="clearf"><a href="#">金融</a></li>
            <li class="clearf"><a href="#">有品</a></li>
            <li class="clearf"><a href="#">小爱开放平台</a></li>
            <li class="clearf"><a href="#">政企服务</a></li>
            <li class="clearf"><a href="#">资质证照</a></li>
            <li class="clearf"><a href="#">协议规则</a></li>
            <li class="download clearf">
              <a href="#" >下载app</a>
              <span class="label-nav">
                <img :src="imgUrl" width="89px" height="89px">
                <span>小米商城app</span>
              </span>
            </li>
            <li class="clearf"><a href="#">Select Region</a></li>
          </ul>
      </div>

      <!-- 右边导航 -->
      <div class="header-right">
          <ul>
            <li class="clearf"><a href="#">登录</a></li>
            <li class="clearf"><a href="#">注册</a></li>
            <li class="clearf"><a href="#">消息通知</a></li>
            <li class="shopcar clearf" >
              <i class="iconfont icon-gouwuche"></i><a href="#">购物车 (<span>{{shopcarNum}}</span>)</a>
              <span class="shopcarCtx">{{ctx}}</span>
            </li>
          </ul>
      </div>

    </div>
</template>

<script>
    export default {
        name: "header",
        data(){
          return{
            Lefttitles : {


            },
            imgUrl:"/static/img/headerdown.png",
            shopcarNum: 0,
            ctx: '购物车中还没有商品，赶紧选购吧！'
          }

        },
      methods:{

      },

    }
</script>

<style scoped>
 #head{
  width: 100%;
  height: 40px;
  background-color: #333;

}

 #head>div{
   float: left;
 }
 /*清除浮动的*/
 .clearf:after{
   display: block;
   content: "";
   clear: both;
 }


  /* 左边导航的样式 */
  .header-left{
    width: 65%;
    height: 100%;
  }

  .header-left ul{
    list-style-type: none;
    font-size: 0;
    line-height: 40px;
    vertical-align: middle;
  }

  .header-left ul li{
    float: left;
    font-size: 13px;
  }

  .header-left ul li a{
    color: #999999;
    text-decoration: none;
    padding: 0 8px;
    border-right: 1px solid #3b423e;
  }

  .header-left ul li:first-child{
    margin-left: 300px ;
  }

  .header-left ul li a:hover{
    color: #FFF;
  }

 .header-left ul .download:hover .label-nav{
   display: block;
 }

  .label-nav{
    display: none;
    position: absolute;
    width: 135px;
    height: 165px;
    left: 910px;
    background-color: #fff;
    box-shadow: rgb(170, 170, 170) 0px 1px 5px;
    transition: 1s;
  }

  .label-nav::before{
    position: absolute;
    top: -10px;
    left: 52px;
    content: '';
    border-left: 10px solid transparent;
    border-right: 10px solid transparent;
    border-bottom: 10px solid #fff;
  }

  .label-nav img{
    width: 95px;
    height: 95px;
    margin: 20px 20px;
    margin-bottom: 0;
  }

  .label-nav span {
    font-size: 17px;
  }
 /* 左边导航的样式*/


 /* 右边导航的样式*/
  .header-right{
    width: 35%;
    height: 100%;
  }

  .header-right ul{
    list-style-type: none;
    font-size: 0;
    line-height: 40px;
    vertical-align: middle;
  }

  .header-right ul li{
    float: left;
    font-size: 13px;
  }

  .header-right ul li a{
    color: #999;
    text-decoration: none;
    padding: 0 8px;
    border-right: 1px solid #3b423e;
  }

  .header-right ul li a:hover{
    color: #fff;
  }

  .header-right ul .shopcar{
      width: 125px;
      height: 40px;
      background-color: #424242;
  }

 .header-right ul .shopcar a{
   border-right: none;
   font-weight: bold;
 }


 .header-right ul .shopcar i{
   color: #fff;
 }

 .header-right ul .shopcar:hover {
    background-color: #fff;
 }

 .header-right ul .shopcar:hover a{
   color: #ff6700;
 }


 .header-right ul .shopcar:hover i{
   color: #ff6700;
 }

 .header-right ul .shopcar:hover .shopcarCtx{
   display: block;
 }

  .header-right ul .shopcar .shopcarCtx{
    display: none;
    position: absolute;
    top: 40px;
    right: 350px;
    width: 335px;
    height: 100px;
    background-color: #fff;
    line-height: 100px;
    vertical-align: middle;
    box-shadow: 0 2px 10px rgba(0,0,0,0.15);
  }

</style>
