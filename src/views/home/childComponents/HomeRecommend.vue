<template>
  <div class="home-recommend">
    <div v-for="item in recommendData" class="home-recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommendView',
  props: {
    recommendData: {
      type: Array,
      default () {
        return [];
      }
    }
  },
}
</script>

<style lang="less" scoped>
.home-recommend {
  display: flex;
  width: 100%;
  border-bottom: 10px solid #eee;
  text-align: center;
  font-size: 12px;

  .home-recommend-item {
    flex: 1;

    a {
      color: #666;

      img{
        width: 70px;
        height: 70px;
        margin-top: 10px;
      }
    }
  }
}
</style>
