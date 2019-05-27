<template>
  <section class="container">
    <div class="banner">
      <cl-banner />
    </div>
    <div class="content">
      <cl-project />
      <cl-docs />
    </div>
  </section>
</template>

<script>
import ClBanner from '~/components/layout/bannar.vue' ;
import ClProject from '~/components/layout/project.vue' ;
import ClDocs from '~/components/layout/docs.vue' ;
import ClMenu from '~/components/layout/menu.vue' ;

export default {
  name: 'Index',
  components: {ClBanner,ClProject,ClDocs,ClMenu},
  data() {
    return {

    }
  },
  mounted() {
  },
  methods: {

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
    font-size: 3rem;
    top: 40vh;
    left: 6rem;
    z-index: 1001;
    opacity: 0.9;
  }
  .moto {
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
    background: url('../assets/banner/bg.png');
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
.content{
  position:relative;
}
</style>
