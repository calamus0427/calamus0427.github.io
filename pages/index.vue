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
.content{
  position:relative;
}
</style>
