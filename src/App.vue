<script setup>
import search from "./components/search.vue"
import top from "./components/top.vue"
import grid from "./components/grid.vue";
import Grid from "@/components/grid.vue";
import fl from "@/components/fl.vue";
import goods from "@/components/goods.vue";
import foot from "@/components/foot.vue"
import slideBar from "@/components/slideBar.vue";

</script>
<template>
  <top style="overflow: hidden"></top>
  <search style="position: sticky;top: 0"></search>
  <fl></fl>
  <div class="content">
    <h3>为你推荐</h3>
  <grid style="position: sticky;top:54px" id="grid"></grid>
    <slideBar></slideBar>
    <goods v-for="i in 5"></goods>
  </div>
  <foot></foot>
</template>


<style scoped>
.content {
  width: 100%;
  background-color: #e3e4e5;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 10px;
}

.content h3 {
  font-size: 28px;
  font-weight: 700;
  margin: 10px 0 30px 0;
}

</style>
