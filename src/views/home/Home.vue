<template>
  <div id="home">
    <nav-bar class="home">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"/>
    <recommend-view :recommends="recommends"/>
    <feature-view/>
  </div>

</template>
<script>
  import NavBar from 'components/common/navbar/NavBar'
  import HomeSwiper from './childComps/HomeSwiper'
  import RecommendView from './childComps/RecommendView';
  import FeatureView from './childComps/FeatureView'
  import {getHomeMultidata} from 'network/home'
 
  export default {
    name: "Home",
    data() {
      return {
        banners: [],
        recommends: []
      }
    },
    methods: {},
    components: {
      NavBar,
      HomeSwiper,
      RecommendView,
      FeatureView
    },
    created() {
      getHomeMultidata().then(res => {
        this.banners = res.data.banner.list;
        this.recommends = res.data.recommend.list
      })
    } 
  }
</script>
<style scoped>
  #home{
    padding-bottom: 50px;
  }
  .home {
    background-color: #FF8198;
    color: white;
  }
</style>