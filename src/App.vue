
<template>
  <div>
    <div class="selector">
      <selector
        placeholder="请选择框架"
      ></selector>
    </div>
    <div class="side-bar">
      <tree-menu>
        <template v-for="item of menuData">
          <menu-item
            v-if="!item.children"
            :key="item.id"
          >{{item.title}}</menu-item>
          <re-sub-menu
            v-else
            :key="item.id"
            :data="item"
          ></re-sub-menu>
        </template>
      </tree-menu>
    </div>
    <div class="container">
      <carousel
        :autoplay="true"
        :duration="3000"
        :initial="3"
        :hasDot="true"
        :hasDirector="true"
        dotBgColor="black"
      >
        <car-item
          v-for="(item, index) of carData"
          :key="index"
        >
          <img :src="'./src/assets/img/' + item.img_name" > 
        </car-item>
      </carousel>
    </div>
  </div>
</template>

<script >
// 传递轮播图数据
import carData from '@/data/carousel';
import menuData from '@/data/menu';

export default{
  name: "App",
  setup(){
    return {
      carData,
      menuData
    }
  }

}
</script>

<style scoped>
.selector{
  margin: 50px auto;
}

.side-bar{
  margin-top: auto;
  width: 300px;
}
.container{
  width: 520px;
  height: 280px;
  margin: 100px auto;
}
</style>
