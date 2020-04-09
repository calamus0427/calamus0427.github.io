<!--
 * @Author       : Calamus
 * @websit       : calamus.xyz
 * @Description  :
 * @FilePath     : /calamus0427.github.io/components/layout/bannar.vue
 * @Date         : 2019-10-31 13:46:41
 * @LastEditors  : Calamus
 * @LastEditTime : 2020-04-09 12:37:05
 -->
<template>
    <div ref="container" class="toolbar_container"        >
      <div class="calamus">
        <a href="//www.calamus.xyz" target="_blank">Calamus</a>
      </div>
      <div class="moto">
        这世界上一定有另一个我，
        <br />
        做着我不敢做的事，
        <br />
        过着我想过的生活。
      </div>
      <div class="filt"></div>
      <div
        ref="inner"
        class="inner"
        @mousemove.native="onMouseMoveHandler"
      ></div>
    </div>
</template>

<script>
export default {
  name: 'bannar',
  data() {
    return {
      x: 0,
      y: 0,
      ox: 0,
      oy: 0,
      counter: 0,
      updateRate: 2,
      content: '',
      loading: false,
      colors: 'red'
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.$refs.container.onmousemove = this.onMouseMoveHandler
      this.setOrigin(this.$refs.container)
    })
  },
  methods: {
    updatePosition(event) {
      const e = event || Window.event
      this.x = (e.clientX - this.ox) / 30
      this.y = (e.clientY - this.oy) / 30
    },
    setOrigin(e) {
      this.ox = e.offsetLeft + Math.floor(e.offsetWidth / 2)
      this.oy = e.offsetTop + Math.floor(e.offsetHeight / 2)
    },
    show() {
      return '(' + this.x + ',' + this.y + ')'
    },
    onMouseMoveHandler(event) {
      if (this.isTimeToUpdate()) {
        this.update(event)
      }
    },
    isTimeToUpdate() {
      return this.counter++ % this.updateRate === 0
    },
    update(event) {
      this.updatePosition(event)
      this.updateTransformStyle(this.x.toFixed(5), this.y.toFixed(5));
    },
    updateTransformStyle(x, y) {
      const style = 'translate(' + (-1)*x + 'px,' + (-2)*y + 'px)'
      this.$nextTick(() => {
        this.$refs.inner.style.transform = style
        this.$refs.inner.style.webkitTransform = style
        this.$refs.inner.style.mozTransform = style
        this.$refs.inner.style.msTransform = style
        this.$refs.inner.style.oTransform = style
      })
    },
    setImgPosition() {
      const innerImg = this.$refs.innerImg
      const width = document.body.clientWidth
      const height = document.body.clientHeight
      const imgHeight = innerImg.offsetHeight
      const marginLeft = -width / 55 + 'px'
      const marginTop = -(imgHeight - height) / 2 / 55 + 'px'
      this.$refs.inner.style.margin = marginTop + ' 0 0 ' + marginLeft
    }
  }
}
</script>

<style lang="less" scoped>
.toolbar_container {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  position: relative;
  .calamus {
    position: absolute;
    top: 40vh;
    left: 6rem;
    z-index: 1001;
    opacity: 0.9;
    font: italic 3em Georgia, serif;
  }
  .moto {
    font-family: 'webfont';
    position: absolute;
    font-size: 1.2rem;
    top: 55vh;
    left: 6rem;
    z-index: 1001;
    color: brown;
    opacity: 0.8;
  }
  .filt {
    position: absolute;
    top: -100px;
    width: 0;
    height: 0;
    border-width: 0 0 30px 30px;
    border-bottom: calc(100vh + 100px) solid #ecb12b52;
    border-right: 70vw solid transparent;
    z-index: 1000;
  }
  .inner {
    position: absolute;
    width: 110%;
    margin-left: -5%;
    height: 110%;
    margin-top: -2%;
    overflow: hidden;
    background: url('https://cdn.calamus.xyz/github/bg.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom right;
    opacity: 1;
    img {
      width: 100%;
    }
  }
}

.cl_toolbar {
  background-color: white;
  border-radius: 0% 0% 50% 50%;
  a {
    text-decoration: none;
    padding: 0 2rem;
    font-size: 16px;
    font-weight: 400;
  }
}
</style>
