<template>

<el-container>
  <el-header>
      <el-row :gutter="20">
        <el-col :span="2"><div class="grid-content bg-purple">
            <el-image :src="img"></el-image>
            </div></el-col>
        <el-col :span="18"><div class="grid-content bg-purple">
            <p></p>
            </div></el-col>
        <el-col :span="2"><div class="grid-content bg-purple">
            <a>登录</a></div>
            </el-col>
        <el-col :span="2"><div class="grid-content bg-purple">
            <a>注册</a></div>
            </el-col>
      </el-row>
      
      
  </el-header>
  <el-main>
      <el-row :gutter="40">
        <el-col :span="8">
            <div class="grid-content bg-purple">
                  <div class="block">
                        <el-carousel>
                        <el-carousel-item v-for="item in 4" :key="item">
                            <h3 class="small"> 
                                <img src="https://assets.dapp.review/image/2020.08.21/dRshQ2CJn5GNtcDTPzF3rHj6HjRXmf5b.jpg">
                            </h3>
                           
                        </el-carousel-item>
                        </el-carousel>
                    </div>
            </div>
        </el-col>
        <el-col :span="8">
            <div class="grid-content bg-purple">
                  <div class="block">
                        <el-carousel >
                        <el-carousel-item v-for="item in 4" :key="item">
                            <h3 class="small"> 
                                <img src="https://assets.dapp.review/image/2020.08.21/dRshQ2CJn5GNtcDTPzF3rHj6HjRXmf5b.jpg">
                            </h3>
                        </el-carousel-item>
                        </el-carousel>
                    </div>
            </div>
        </el-col>
        <el-col :span="8">
            <div class="grid-content bg-purple">
                  <div class="block">
                        <el-carousel >
                        <el-carousel-item v-for="item in 4" :key="item">
                            <h3 class="small"> 
                                <img src="https://assets.dapp.review/image/2020.08.21/dRshQ2CJn5GNtcDTPzF3rHj6HjRXmf5b.jpg">
                            </h3>
                        </el-carousel-item>
                        </el-carousel>
                    </div>
            </div>
        </el-col>
      </el-row>

  </el-main>
  <el-main class="top">
      <h1>热门推荐</h1>
      <el-row>
          <el-col :span="8" v-for="o in 6" :key="o">  
            <el-card >
            <img :src="img" class="image">
            <span> {{'Aragon ' + o }}</span>
            <div style="padding: 0px;">
                <div class="bottom clearfix">
                <span class="time">{{ doc }}</span>
                </div>
                <el-row>
                     <el-col :span="6">
                        <i class="i-logo el-icon-success"></i>
                     </el-col>
                     <el-col :span="6">
                        <i class="i-logo el-icon-s-management"></i>
                     </el-col>
                    <el-col :span="6">
                        <i class="i-logo el-icon-share"></i>
                     </el-col>
                    <el-col :span="6">
                        <i class="i-logo el-icon-delete"></i>
                     </el-col>
                </el-row>

            </div>
            </el-card>            
 
            </el-col>
      </el-row>
  </el-main>
  <el-main>
      <h1>推荐热文</h1>
      <el-row>
        <el-col :span="8">
            <el-card shadow="hover">
                <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"  >
                 <div style="padding: 4px;">
                    <span>ANT 币值涨了50%</span>
                    <div class="bottom clearfix">
                        <el-button type="text" class="button">查看全部</el-button>
                    </div>
                   </div>
            </el-card>
            </el-col>
        <el-col :span="8">
            <el-card shadow="hover">
                <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"  >
                 <div style="padding: 4px;">
                    <span>ANT 币值涨了50%</span>
                    <div class="bottom clearfix">
                        <time class="time">{{ currentDate }}</time>
                        <el-button type="text" class="button">查看全部</el-button>
                    </div>
                   </div>
            </el-card>
            </el-col>
        <el-col :span="8">
            <el-card shadow="hover">
                <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" >
                 <div style="padding: 4px;">
                    <span>ANT 币值涨了50%</span>
                    <div class="bottom clearfix">
                        <time class="time">{{ currentDate }}</time>
                        <el-button type="text" class="button">查看全部</el-button>
                    </div>
                   </div>
            </el-card>
            </el-col>
        </el-row>
  </el-main>

  <el-main class="banner-main">
      <h1>巨大的banner位</h1>
  </el-main>

    <el-main class="vide-main">
        <h1>热门视频</h1>
        <el-row :gutter="20">
            <el-col :span="6"><div class="grid-content bg-purple">
                <el-image :src="video"></el-image>
                </div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple">
                <el-image :src="video"></el-image>
                </div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple">
                <el-image :src="video"></el-image>
                </div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple">
                <el-image :src="video"></el-image>
                </div></el-col>
        </el-row>
     
  </el-main>
  <el-footer>© 2020 Daogle</el-footer>
</el-container>
    
</template>
<script>
export default {
    data(){
        return {
            doc:"Aragon 是以太坊区块链上的一个可以让任何人创建和管理任意组织，如公司、开源项目、非政府组织、基金会、对冲基金等的 DApp",
            img: "https://assets.website-files.com/5e997428d0f2eb13a90aec8c/5e99778310343ed2dfe89331_logo_big.svg",
            video: "https://assets.dapp.review/image/2020.08.24/LAND-presale-191111-1.2020-08-20%2012_24_49.gif",
        }
    }
}
</script>
<style scoped>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
    .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }

   body > .el-container {
    margin-bottom: 40px;
  }

    .el-carousel__item h3 {
 
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    
     background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
      
     background-color: #d3dce6;
  }
  .el-carousel {
    border-radius: 8%;
    margin: 40px;
   
  }

  .top {
      background: #FFF;
  }


/* card */
  .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }

  .image {
      margin: 0 auto;
      width: 50%;
      border-radius: 50%;
  }

  .el-card {
      margin: 50px;
  }
  
  .el-col  {
      font-size: 30px;
  }

  /* banner-main */
  .banner-main {
       background: rgb(201, 196, 196);
  }


  /* video-main */
  .vide-main {
      background: rgb(27, 27, 27);
      color: whitesmoke;
  }

  .el-footer {
      background: rgb(27, 27, 27);
      color: whitesmoke;
  }

  /* header */
  .el-header a{
      font-size: 18px;
  }
</style>