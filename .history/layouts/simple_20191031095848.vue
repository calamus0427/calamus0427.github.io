<template>
  <div>
    <nuxt />
  </div>
</template>

<script>
import ClFooter from '~/components/layout/footer.vue' ;
export default {
  components:{ClFooter}
}
</script>

<style lang="less">
//animation
@keyframes windyX {
    from {
        transform-origin: 50% 0;
        transform: rotate(0deg);
    }

    25% {
        transform-origin: 50% 0;
        transform: rotate(-45deg);
    }

    62% {
        transform-origin: 50% 0;
        transform: rotate(30deg);
    }

    83% {
        transform-origin: 50% 0;
        transform: rotate(-15deg);
    }

    95% {
        transform-origin: 50% 0;
        transform: rotate(5deg);
    }

    to {
        transform-origin: 50% 0;
        transform: rotate(0deg);
    }
}

@keyframes textConcatIn {
    0% {
        letter-spacing: 1em;
        transform: translateZ(400px);
        opacity: 0;
    }

    40% {
        opacity: 0.6;
    }

    100% {
        transform: translateZ(0);
        opacity: 1;
    }
}

@keyframes rotate3dTurnOutX {
    0% {
        transform: rotateX(0deg) scale(1);
        opacity: 1;
    }

    80% {
        opacity: 0;
    }

    100% {
        transform: rotateX(360deg) scale(0);
    }
}

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

@font-face {
  font-family: 'webfont';
  font-display: swap;
  src: url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.eot'); /* IE9*/
  src: url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
  url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.woff2') format('woff2'),
  url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.woff') format('woff'), /* chrome、firefox */
  url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.ttf') format('truetype'), /* chrome、firefox、opera、Safari, Android, iOS 4.2+*/
  url('//at.alicdn.com/t/webfont_1tmu1xfmg5t.svg#杨任东竹石体-Bold') format('svg'); /* iOS 4.1- */
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

a{
  color: #6b4b47!important;
  cursor: pointer;
  text-decoration: none;
  font-weight: 500;
  &:hover{
     color: #6b4b4730 !important;
  }
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
