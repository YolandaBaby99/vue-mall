<template>
  <div class="goods">
    <goods-list-item v-for="(item,index) in goodsList" :key="index" :goods-item="item" />
    <!-- {{goods}} -->
  </div>
</template>

<script>
import GoodsListItem from "./GoodsListItem";
export default {
  name: "GoodsList",
  components: {
    GoodsListItem
  },
  props: {
    goodsList: {
      type: Array,
      default() {
        return [];
      }
    }
  }
};
</script>

<style scoped>
.goods {
   display: flex;
   flex-wrap: wrap;
   justify-content: space-around;
}
</style>