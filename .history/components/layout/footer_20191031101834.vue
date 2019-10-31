<template>
      <footer
        >
        <div class="container_arrow">
          <div class="container">

            <div class="message">
              <p>♫ Hi ♫</p>
            </div>

            <div class="cat">
              <span class="eyes left"></span>
              <span class="eyes right"></span>
              <span class="mouth"></span>
            </div>

          </div>
        </div>
        <div class="contract">
          <div class="left">
            <p>
              <img src="https://cdn.calamus.xyz/leimu.jpeg" alt="">
            </p>
            <p>专注前端开发的二次元美少女</p>
            <p>
              <a href="https://www.calamus.xyz/" target="_blank">主站</a>
              <a href="http://github.com/calamus0427" target="_blank">github</a>
              <a href="https://www.cnblogs.com/calamus" target="_blank">blog</a>
              <a href="http://calamus.wiki/daily-FE/" target="_blank">每日前端</a>
              <a href="http://calamus.wiki/#/" target="_blank">关于我</a>
            </p>
          </div>
          <div class="right">
            <p>email： <a href="kiz.calamus@gmail.com">kiz.calamus@gmail.com</a>
              </p>
            <p>
              <img src="https://cdn.calamus.xyz/qq%E7%BE%A4.png" alt="">
              <img src="https://cdn.calamus.xyz/wechat.jpg" alt="">
            </p>
          </div>
        </div>
        <div
            class="copyright"
          >
                Copyright &copy; 2015-2019 <a href="//www.calamus.xyz">Calamus</a>
        </div>
    </footer>

</template>

<script>
export default {
    name:'okr-footer',
    data(){
        return {
        }
    }
}
</script>

<style lang="less" scoped>
@keyframes spinner {
    from {
        transform: rotate(0deg);
    }

    to {
        transform: rotate(360deg);
    }
}
@keyframes jump {

    from,
    10% {
        transform: translateY(0) scale3d(1, 1, 1);
    }

    30% {
        transform: translateY(10%) scale3d(1.05, .8, 1);
    }

    50% {
        transform: translateY(-50%) scale3d(1, 1.1, 1);
    }

    65% {
        transform: translateY(0) scale3d(1, 1, 1);
    }

    75% {
        transform: translateY(8%) scale3d(1.08, .84, 1);
    }

    85% {
        transform: translateY(6%) scale3d(1.05, .88, 1);
    }

    90%,
    to {
        transform: none;
    }
}

.container,.message,.cat {
    display: block;
    position: absolute;
    margin: auto; padding: 0;
    top: -60px; bottom: 0; left: 0; right:0;
}

// span, li{ font-family: 'Petit Formal Script', cursive; text-align: center; }

.container{
  background: white;
  height: 100px;
  width: 100px;
  border-radius: 50%;
  border: 4px solid #FAF4E2;
  overflow: hidden;
}

.cat {
  background:#73635D;
  height: 60%;
  top: auto;
  bottom: 0;
  width: 60px;
  z-index: 0;
}

.cat:before, .cat:after {
    width: 0;
    height: 0;
    top: -18px;
    position: absolute;
    content: "";
}

.cat:before{
    border-left: 0px solid transparent;
    border-right: 20px solid transparent;
    border-bottom: 20px solid #73635D;
    left: 0;
}

.cat:after{
    border-right: 0px solid transparent;
    border-left: 20px solid transparent;
    border-bottom: 20px solid #73635D;
    right: 0;
}

.cat .eyes{
  position: absolute;
  height: 10px; width: 10px;
  background: #FFF;
  border-radius: 100%;
  top: 15px;
}

.cat .eyes.left{ left: 12px; }
.cat .eyes.right{  right: 12px; }

.cat .mouth{
  position: absolute;
  height: 3px; width: 60%;
  background: #eee;
  border-radius: 0 0 30% 30%;
  top: 35px;
  margin: auto;
  left: 0; right: 0;
}

.container:hover .cat .mouth{
  height: 10px; width: 10px;
  border-radius: 0 0 50% 50%;
  top: 35px;
}

.message{
  background: transparent;
  // height: 20px;
  // width: 50px;
  padding: 2px;
  bottom: auto; top: 12px;
  transition: opacity 0.5s;
  -webkit-transition: opacity 0.5s;
  opacity:0;
}

.container:hover .message{
  opacity: 1;
}

.message p {
	font-family: Helvetica, Verdana, sans-serif;
  font-size: 0.5em;
	text-align: center;
}

.message:after {
    width: 0;
    height: 0;
    border-right: 10px solid transparent;
    border-left: 10px solid transparent;
    border-top: 10px solid #FFFFFF;
    bottom: -10px;
    right: 30px;
    position: absolute;
    content: "";
}



footer{
    background: linear-gradient(to left,#F6E3B7,#FBFBF3);
    background: #FAF4E2;
    width: 100%;
    margin-top:100px;
    .container_arrow{
      min-height:60px;
      position: relative;
    }
    .contract{
      display:flex;
      font-family: "Bad Script", cursive;
      .left{
        width:50%;
        text-align:right;
        padding-right:8rem;
        p:nth-child(1){
          img{
            width:60px;
            border-radius: 50%;
            &:hover{
              animation: spinner 1000ms both;
            }
          }
        }

      }
      .right{
        width:50%;
        padding-left:8rem;
        p:nth-child(2){
          // display:flex;
          img{
            // display:inline-block;
            width:120px;
            &:hover{
              animation: jump 1000ms both
            }
          }
        }
      }
    }
    .copyright{
      position: relative;
      height:35px;
      line-height:35px;
      text-align: center;
      &:before{
        position: absolute;
        top: 0px;
        left: 50%;
        display: block;
        width: 80%;
        height: 1px;
        margin-left: -40%;
        content: "";
        background: radial-gradient(ellipse at center,rgba(0,0,0,.2) 0,hsla(0,0%,100%,0) 75%);
        background: -moz-radial-gradient(ellipse at center,rgba(0,0,0,.2) 0,hsla(0,0%,100%,0) 75%);
      }
    }

}
</style>


