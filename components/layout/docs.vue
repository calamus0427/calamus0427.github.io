<template>
  <div>
      <div class="box11_ribbon">文章</div>
      <a-timeline mode="alternate">
        <a-timeline-item>
          <a-icon slot="dot" type="laptop" style="font-size: 16px;color: #6b4b47" />
          <div>
            <a href="http://calamus0427.github.io/docs/vue/introduce/#/" target="_blank" class="title" >vue从入门到女装</a>
            <p class="content">Vue+element从零开始搭建管理后台 👻</p>
            <p class="img_des"><img src="https://cdn.calamus.xyz/snapshots/vue-element.gif" alt=""></p>
          </div>
        </a-timeline-item>
        <a-timeline-item>
          <a-icon slot="dot" type="crown" style="font-size: 16px;color: #6b4b47" />
          <div>
            <a  href="http://calamus0427.github.io/docs/Taro/introduce/#/" target="_blank" class="title">Taro从入门到女装</a>
            <p class="content">三端统一框架 💯 Taro学习笔记 🙌</p>
            <p class="img_des"><img src="https://cdn.calamus.xyz/snapshots/Taro.png" alt=""></p>
          </div>
        </a-timeline-item>
        <a-timeline-item>
          <a-icon slot="dot" type="crown" style="font-size: 16px;color: #6b4b47" />
          <div>
            <a  href="http://calamus0427.github.io/docs/uni-app/introduce/#/" target="_blank" class="title">uni-app从入门到女装</a>
            <p class="content">跨端统一框架 💯 uni-app学习笔记 🙌</p>
            <p class="img_des"><img src="https://cdn.calamus.xyz/snapshots/uni.png" alt=""></p>
          </div>
        </a-timeline-item>
        <a-timeline-item>
          <a-icon slot="dot" type="compass" style="font-size: 16px;color: #6b4b47" />
          <div>
            <a  href="http://calamus0427.github.io/docs/233point/introduce/#/" target="_blank" class="title">233次元介绍</a>
            <p class="content">来打破次元壁吧 😪</p>
            <p class="img_des"><img src="https://cdn.calamus.xyz/snapshots/233point.png" alt=""></p>

          </div>
        </a-timeline-item>
        <a-timeline-item>
          <a-icon slot="dot" type="tablet" style="font-size: 16px;color: #6b4b47" />
          <div>
            <a  href="http://calamus0427.github.io/calamus-wechat/#/" target="_blank" class="title">小程序开发经验分享</a>
            <p class="content">小程序开发填坑记录 😪</p>
            <p class="img_des"><img src="https://cdn.calamus.xyz/snapshots/wechat.png" alt=""></p>

          </div>
        </a-timeline-item>
      </a-timeline>
  </div>
</template>

<style lang="less" scoped>

.box11_ribbon{
    margin: 2rem auto;
    width: 200px;
    height: 40px;
    background: -webkit-gradient(linear, 555% 20%, 0% 92%, from(rgba(0, 0, 0, 0.1)), to(rgba(0, 0, 0, 0.0)), color-stop(.1,rgba(0, 0, 0, 0.2)));
    border-left: 1px dashed rgba(0, 0, 0, 0.1);
    border-right: 1px dashed rgba(0, 0, 0, 0.1);
    -webkit-box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.2);
    text-align:center;
    line-height:40px;
    font-size:1rem;
    font-weight:500;
    color:burlywood;
    cursor:pointer;
    &:hover{
        animation: textConcatIn 1000ms both
    }
}
.img_des{
  img{
    width:50%;
  }
}
</style>

