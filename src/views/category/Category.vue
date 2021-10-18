<template>
  <nav-bar>
    <div slot="left" class="left">
      <a href="#">
        <img src="~assets/images/category/back.svg" alt="">
      </a>
    </div>
    <div slot="center" class="searchText">
      <div class="textIcon">
          <img src="~assets/images/category/search.svg" alt="">
      </div>
      <div class="textInput">
        <input type="text" name="" id="" v-model="textData">
      </div>
    </div>
    <div slot="right">
      <a href="#" class="searchBtn">
        <span>搜索</span>
      </a>
    </div>
  </nav-bar>
</template>
<script>
import NavBar from 'components/common/navbar/NavBar'

export default {
  name: "Category",
  data () {
   return {
     textData:'女装'
   }
  },
   methods:{},
   components:{NavBar}
}
</script>
<style scoped>
.left{
  text-align: center;
}
.left img{
  width: 24px;
  height: 24px;
  margin: 11px 0;
}
.searchText{
  display: flex;
  background-color: #F7F7F7;
  border-radius: 30px;
  height: 36px;
  margin-top: 5px;
}
.textInput{
  position: relative;
  width: 140px;
}
.textInput input{
  position: absolute;
  right: 5px;
  top: 9px;
  flex: 1;
  width: 120px;
  height: 20px;
  border: none;
  background-color: #F7F7F7;
}
.textIcon{
  position: relative;
  width: 40px;
  text-align: center;
}
.textIcon img{
  position: absolute;
  width: 20px;
  right: 0;
  top: 8px;
}
.searchBtn span{
  padding: 5px;
  background-color: #E93B3D;
  border-radius: 5px;
  color: #fff;
}


</style>