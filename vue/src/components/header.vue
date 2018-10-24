<template>
  <div class="header">
    <div class="left">
      <img class="headerImg-left" src="../../static/image/header1.png" alt="">
    </div>
    <div class="des" v-if="showDesFlag" v-html="des[1]" ></div>
    <div class="avater"></div>
    <div class="right">
      <img class="headerImg-right" src="../../static/image/header2.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'transfer',
  data () {
    return {
      des:[
        "希望有一天你会变成特别优秀的人" ,
        "这世界上</br>一定有另一个我</br>做着我不敢做的事</br>过着我想过的生活"
      ],
      showDesFlag:false
      }
  },
  mounted(){
    this.Trim(this.des[1]);
    setTimeout(this.showDes,3000)
  },
  methods:{
    Trim(str) {  //str表示要转换的字符串
      str =  str.replace(/\n|\r\n/g,"</br>");
      console.log(str)
    },
    showDes(){
      this.showDesFlag = true;
    }
  }
}
</script>

<style scoped>
@keyframes bounceInLeft {
  from {
    opacity: 0;
    transform: translate3d(-100%, 0, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

@keyframes bounceInRight {
  from {
    opacity: 0;
    transform: translate3d(100%, 0, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}
.header{
  position: relative;
}
.des{
    position: absolute;
    top: 200px;
    left: 50%;
    width:300px;
    word-wrap: break-word;
    margin-left: -150px;
    text-align: center;
    z-index: 2;
    font-weight: 300;
    color: #8e8c8c;
    margin-top: 10px;
    font: italic 20px/1.3em Georgia,serif;
    font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
    font-style: normal;

}
.left,.right{
  width:100%;
  position: relative;
}
.left img{
  position: absolute;
  top:30px;
  left:170px;
}
.right img{
  position: absolute;
  top:270px;
  right:170px;
}
.left{
  animation: bounceInLeft 3s
}
.right{
  animation: bounceInRight 3s
}
</style>
