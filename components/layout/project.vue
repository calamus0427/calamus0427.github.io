<template>
<section>
  <div class="box11_ribbon">项目</div>
  <div class="project_card">
      <cl-cards  v-for="(item,index) in projectList" :key="index" :img="index" :title="item.title" class="project_card_item">
              <ul v-if="item.children">
                <li v-for="(cItem,index2) in item.children" :key="index2">
                    <a :href="cItem.src" target="_blank">{{cItem.title}}</a>
                </li>
              </ul>
      </cl-cards>
    </div>
</section>

</template>

<script>
import ClCards from '../cards'
export default {
  name: 'project',
  components:{ClCards},
  data: () => ({

      projectList:[
        {
          title:'vue项目',
          src:'javascript:;',
          des:'',
          img:'',
          children:[
            {
              title:'vue-element后台项目',
              src:'//calamus.wiki/vue-element-admin-calamus/#/login',
              des:'',
              img:'',
            },
            {
              title:'vue博客',
              src:'//calamus.wiki/my-blog/#',
              des:'',
              img:'',
            },
            {
              title:'vue cli v3 + d3.js',
              src:'//calamus.wiki/vue-d3/#/',
              des:'',
              img:'',
            },{
              title:'MeowUI 组件库',
              src:'//calamus.wiki/MeowMeowUI/',
              des:'',
              img:'',
            },
            {
              title:'基于vue和svg实现的树形图ui',
              src:'//github.com/calamus0427/vue-svg-tree',
              des:'',
              img:'',
            }
          ]
        },{
          title:'小游戏',
          src:'javascript:;',
          des:'',
          img:'',
          children:[
            {
              title:'五子棋游戏',
              src:'https://calamus0427.github.io/calamus_game/Backgammon',
              des:'',
              img:'',
            },
            {
              title:'2048游戏',
              src:'https://calamus0427.github.io/calamus_game/2048',
              des:'',
              img:'',
            },
            {
              title:'俄罗斯方块游戏',
              src:'https://calamus0427.github.io/calamus_game/canvas/guaguale/demo1/',
              des:'',
              img:'',
            },
            {
              title:'贪吃蛇游戏',
              src:'https://calamus0427.github.io/calamus_game/eatSnake',
              des:'',
              img:'',
            },
            {
              title:'canvas写字',
              src:'https://calamus0427.github.io/calamus_game/canvas/word',
              des:'',
              img:'',
            },
            {
              title:'东边的山坡上有两头牛',
              src:'https://calamus0427.github.io/calamus_game/canvas/guaguale/demo1/',
              des:'',
              img:'',
            }
          ]
        },{
          title:'小程序',
          src:'javascript:;',
          des:'',
          img:'',
          children:[
            {
              title:'233次元',
              src:'//github.com/233point',
              des:'',
              img:'',
            },
            {
              title:'订餐小程序',
              src:'//www.cnblogs.com/calamus/p/9675213.html',
              des:'',
              img:'',
            }
          ]
        },{
          title:'其他',
          src:'javascript:;',
          des:'',
          img:'',
          children:[
            {
              title:'CSS3动画演示',
              src:'//calamus.wiki/css3-transition/css3-transition/',
              des:'',
              img:'',
            },
            {
              title:'live2d网页看板娘',
              src:'javascript:;',
              des:'',
              img:'',
            },
            {
              title:'live2d网页看板娘',
              src:'//calamus.wiki/calamus-live2d/demo/',
              des:'',
              img:'',
            },
            {
              title:'常用js代码',
              src:'//github.com/calamus0427/commonJS',
              des:'',
              img:'',
            },
            {
              title:'angular尝试',
              src:'//github.com/calamus0427/launchPad',
              des:'',
              img:'',
            },
            {
              title:'live2d网页看板娘',
              src:'//github.com/calamus0427/page404',
              des:'',
              img:'',
            },
          ]
        }
      ]
  }),
  methods:{

  }
}
</script>

<style lang="less" scoped>
.project_card{
  ul {
      list-style: none;
      li{
        ul{
          margin-left:2rem;
        }
        a{
            text-shadow: 5px 5px 5px #80808087;
            &:hover{
              color: #504D4D;
              font-weight: bold;
              text-decoration: none;
              text-shadow: 5px 5px 5px gray;
            }
        }
      }
  }
}
.project_card{
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  .project_card_item{
    width:18%;
    margin-bottom:2rem;
    margin-top:2rem;
  }
}
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
</style>
