<template>

  <el-container>
    <el-header>
      <el-row :gutter="20">
        <el-col :span="2">
          <div class="grid-content bg-purple">
            <el-image :src="img"></el-image>
          </div>
        </el-col>
        <el-col :span="18">
          <div class="grid-content bg-purple">
            <p></p>
          </div>
        </el-col>
        <el-col :span="2">
          <div class="grid-content bg-purple">
            <a>登录</a></div>
        </el-col>
        <el-col :span="2">
          <div class="grid-content bg-purple">
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
      </el-row>

    </el-main>


    <el-main class="top">
      <h1>热门推荐</h1>
      <el-row :gutter="250">
        <el-col :span="8" v-for="dao in daos" :key="dao.name">
          <el-card shadow="never" body-style="height:300px;">
            <img :src="img" class="image">
            <span class="top-title"> {{ dao.name }}</span>
            <div style="padding: 0px;">
              <div class="bottom clearfix">
                <span class="time">{{ dao.doc }}</span>
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


    <el-main class="top">
      <h1>推荐热文</h1>
      <el-button type="text" style="position: absolute; right:1%">查看更多<i class="el-icon-caret-right"></i></el-button>

      <el-row :gutter="20">
        <el-col :span="6" v-for="o in 4" :key="o">
          <el-card body-style="height:420px; padding:0px; position:relative;">
            <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"
                 style="width:100%; height:250px">
            <span class="hot-new-title"> 阿里股价涨破100美元</span>
            <div style="padding: 0px;">
              <div class="hot-new-content bottom clearfix">
                <span class="time">{{ doc }}</span>
              </div>
            </div>
            <div class="hot-bottom">
              <img :src="img" style="width:40px">
              <el-button type="text" class="button" style="color: #999999;">查看全部</el-button>
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
        <el-col :span="6" v-for="o in 4" :key="o">
          <el-card body-style="height:350px; padding:0px; position:relative;">
            <el-image :src="video"></el-image>
            <span class="hot-new-title">CSGO年度精彩时刻
            </span>
            <div class="hot-bottom" style="margin-top: 130px">
              <div style="color: #999999;"><i class="el-icon-star-off"></i>4794</div>
            </div>
          </el-card>
        </el-col>
      </el-row>
      <section>
        <div class="company">
          <div class="company-logo"></div>
          <div class="company-text">
            <a>加入我们</a>
            <a>联系我们</a>
            <a>更多内容</a>
            <a>友情链接</a>
          </div>
        </div>
      </section>
    </el-main>
    <el-footer class="company-info">© 2020 Daogle.com</el-footer>
  </el-container>

</template>
<script>
export default {
  data() {
    return {
      daos : [
        {name: "YangDAO", doc:"主要由Yang Gang成员组成的DAO，目前主要处理Yang Gang的一些发展项目，成员可在上面对项目的资助进行投票表决，也可以发起自己的项目并请求资助，他们希望随着YangDao的到来与发展，最终能利用这个工具复兴人类繁荣，并为人们带来新的启迪。", icon:""},
        {name: "RaidGuild", doc:"帮助他人建构自己的Web3产品的去中心化团队，服务范围有：提供咨询服务，像验证你的想法，给你的产品一些建构，运营以及发展的建议；给出设计建议，像调整产品市场指向，在写代码前敲定你的UX；提供全栈开发，帮助你实现dApp，建构合约或者前端；市场营销，提升你的模因游戏水平，为你的品牌或者产品构建一个吸引人的故事等。\n" +
            "       他们犹如一个去中心化的雇佣兵团队，准备斩杀一切阻碍你的Web3产品的恶魔。" },
        {name: "DAORecords", doc:"一个旨在将唱片公司去中心化的公司，目前采用将传统sa公司商业模式和DAO结合的方式运作，希望能充分激励艺术家创作，同时促进粉丝消费以及将其他的盈利活动效益最大化。" },
        {name: "Metagame", doc:"Metagame总体上讲是一个大型线上协调“游戏”，也可理解为一个由自由职业者、去中心化组织和资金组成的开源框架，旨在以最小的阻力和尽可能有趣的方式来协调各方创造的价值及其交换。" },
        {name: "dOrg", doc:"dOrg是一个建立在Web3上，且基于Web3运作的全栈自由职业者代理公司，其目的主要在于推动Web3及其生态系统的迭代与成熟。dOrg还促成了第一个基于区块链的责任有限公司 Blockchain-Based Limited Liability Company (BB-LLC)，对于未来利用DAO成立公司有特殊意义。" },
        {name: "Collab19", doc:"Collab19是一个由 MetaCartel 社区成员发起的DAO。它起源于新冠疫情，希望用 DAO 来优化传统慈善事业的诸多问题，从而更好地帮助那些需要帮助的人。然而，抗击疫情仅仅是 Collab19 的开始，Collab19的目标在于降低 DAO 的参与成本，将 DAO 扩展到社会协调中去，让 DAO 发挥更大的社会价值。正如 Collab19 所说：Voting is the new Like！" },

      ],
      doc: "Aragon 是以太坊区块链上的一个可以让任何人创建和管理任意组织，如公司、开源项目、非政府组织、基金会、对冲基金等的 DApp",
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

  .el-main > h1 {
    margin-left: 2rem;
    line-height: 0;
    text-align: left;

  }

  .Note{
    display:-webkit-box;
    text-overflow:ellipsis;
    overflow:hidden;
    -webkit-line-clamp: 2;
    -webkit-box-orient:vertical;
  }

  .hot-new-title {
    position: absolute;
    left: 15px;
    top: 200px;
    font-size: 20px;
    font-weight: 600;
  }

  .hot-new-content {
    position: absolute;
    top: 290px;
    text-align: start;
    left: 15px;
  }

  .hot-new-content > span.time {
    line-height: 22px;
    font-size: 14px;
  }

  .hot-bottom {
    position: relative;
    margin-top: 100px;
  }

  .hot-bottom img {
    position: absolute;
    bottom: 4px;
    left: 5px;
  }

  .hot-bottom button {
    position: absolute;
    bottom: 10px;
    right: 10px;
  }

  .hot-bottom div {
    font-size: 14px;
    font-weight: 600;
    position: absolute;
    bottom: 10px;
    right: 10px;
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

  .row-bg {
    padding: 10px 0;
  }

  .company-text {
    float: right;
  }

  .company-text > a {
    font-size: 20px;
    color: white;
    font-weight: bolder;
    margin-right: 60px;
  }

  .company-info {
    text-align: left;
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

  .top .el-card {
    border: none;
  }

  .top-title {
    font-weight: 700;
    line-height: 1;
    font-size: 18px;
    display: block;
    margin: 15px 0 15px 0;
  }

  .el-main.top .el-row:nth-child(2) {
    line-height: 100px;
  }

  /* card */
  .time {
    font-size: 13px;
    color: #999;
    line-height: 28px;
    font-weight: 400;
    display:-webkit-box;
    text-overflow:ellipsis;
    overflow:hidden;
    -webkit-line-clamp: 3;
    -webkit-box-orient:vertical;
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
    height: 100px;
    width: 100px;
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

  .el-col {
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
  .el-header a {
    font-size: 18px;
  }
</style>
