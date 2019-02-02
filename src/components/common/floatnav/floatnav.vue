<template>
  <div class="fnav">
    <ul>
      <li>
        <a href=""><i class="iconfont icon-19"></i><span>手机APP</span></a>
        <span class="fdown">
          <img :src="imgUrls" alt="" >
          <span>手机扫一扫一分赢好礼</span>
        </span>
      </li>
      <li><a href=""><i class="iconfont icon-geren"></i><span>个人中心</span></a></li>
      <li><a href=""><i class="iconfont icon-kefu"></i><span>联系客服</span></a></li>
      <li><a href=""><i class="iconfont icon-iconset0308"></i><span>购物车</span></a></li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: "body",
      data(){
          return{
            imgUrls: "/static/img/phonedown2.png"
          }
      }
    }
</script>

<style scoped>
 .fnav{
   position: fixed;
   top: 350px;
   right: 0;
   width: 90px;
   height: 380px;
   z-index: 999;

 }

  .fnav ul{
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    list-style-type: none;
    border-top: 1px solid #f5f5f5;
  }

  .fnav ul li{
    width: 100%;
    height: 25%;
    border: 1px solid #f5f5f5;
    border-top: none;
  }

  .fnav ul li:first-child:hover .fdown{
    display: block;
  }

  .fnav ul li:hover a{
    color: #ff6700;
  }

  .fnav ul li .fdown{
    display: none;
    position: absolute;
    width: 138px;
    height: 200px;
    top: 0px;
    right: 95px;
    border: 1px solid #f5f5f5;
  }

 .fnav ul li .fdown img{
   width: 100px;
   height: 100px;
   margin: 20px 15px;
   margin-bottom: 0px;
 }

 .fnav ul li .fdown span{
    display: block;
    width: 85px;
   margin: 17px 25px;
   font-size: 15px;
   color: #999;
 }

  .fnav ul li a{
    width: 100%;
    height: 100%;
    text-decoration: none;
    color: #999;
  }

  .fnav ul li a i{
    display: block;
    margin-top: 15px;
    font-size: 30px;
  }

  .fnav ul li a span{
    display: block;
    margin-top: 15px;
    font-size: 16px;
  }
</style>
