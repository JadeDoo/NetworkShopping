<template>
  <div class="shopping-mall">
    <!-- search bar layout -->
    <div class="search-bar">
       <van-row>
        <van-col span="3">
          <img :src="localtionIcon" alt="" width="70%" class="localtion-icon">
        </van-col>
        <van-col span="16">
          <input type="text" class="search-input">
        </van-col>
        <van-col span="5">
          <van-button size="mini" class="search-btn">搜索</van-button>
        </van-col>
      </van-row>
    </div> 
    <!-- swipe area -->
    <div class="swipe-area">
      <van-swipe :autoplay="1000">
        <van-swipe-item v-for="(banner,index) in bannerPicArray" :key="index">
          <img :src="banner.imageUrl" width="100%" alt="">
        </van-swipe-item>
      </van-swipe>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "Shopping Mall",
      localtionIcon:require('../../assets/images/localtion.png'),
      bannerPicArray:[
        {imageUrl:require('../../assets/images/simleVueDemoPic001.jpg')},
        {imageUrl:require('../../assets/images/simleVueDemoPic002.jpg')},
        {imageUrl:require('../../assets/images/simleVueDemoPic003.jpg')}
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.shopping-mall{
  .search-bar{
    height:2.2rem;
    background-color: #e5017d;
    line-height: 2.2rem;
    .localtion-icon{
      padding-top: .2rem;
      padding-left: .3rem;
    }
    .search-input{
      width: 100%;
      height: 1.3rem;
      border-top: none;
      border-left: none;
      border-right: none;
      border-bottom: 1px solid #fff !important;
      background-color: #e5017d;
      color: #fff;
    }
    .search-btn{
      margin-left: .5rem;
    }
  }
  .swipe-area{
    width: 20rem;
    clear: both;
  }
}
  
</style>


