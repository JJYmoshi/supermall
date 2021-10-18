<template>
  <div class="commend">
    <div v-for="(item,index) in recommends" :key="index" class="commend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>
          {{item.title}}
        </div>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  name: "RecommendView",
  data () {
   return {}
  },
  props:{
    recommends:{
      type:Array,
      default(){
        return []
      }
    }
  },
  methods:{}
}
</script>
<style scoped>
.commend{
  display: flex;
  text-align: center;
  font-size: 12px;
  padding: 10px 0 20px;
  border-bottom: 8px solid #eee;
}
.commend-item{
  flex: 1;
}
.commend-item img{
  width: 70px;
  height: 70px;
  margin-bottom: 10px;
}
</style>