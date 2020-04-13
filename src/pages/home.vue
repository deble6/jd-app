<template>
  <div>
    <el-container>
      <el-header height="60px">

        <div class="user-info">
          <span>admin</span>
        </div>
      </el-header>

      <el-container>
        <!-- <el-aside width="200px">
          <el-menu @select="handlerSelect">
            <el-menu-item v-for="(item, index) in menuList" :index="item.path" :key="index">
              <span slot="title">{{item.title}}</span>
            </el-menu-item>
          </el-menu>
        </el-aside> -->

        <el-main>
          <router-view></router-view>
        </el-main>
      </el-container>

    </el-container>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      menuList: [
        {title: '用户管理', path: '/user-manage'},
        {title: '菜单管理', path: '/menu-manage'},
        {title: '商品管理', path: '/comm-manage'},
        {title: '首页轮播图管理', path: '/home-pic-manage'},
        {title: '商品分类管理', path: '/comm-classify-manage'},
        {title: '客户管理', path: '/client-manage'},
        {title: '订单管理', path: '/order-manage'},
        {title: '热门位商品管理', path: '/hot-comm-manage'},
        {title: '门店信息管理', path: '/shop-info-manage'},
        {title: '司机信息管理', path: '/driver-info-manage'}
      ]
    }
  },
  methods: {
    handlerSelect (key, path) {
      if (key !== this.$route.path) {
        this.$router.replace({path: key})
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.el-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgb(242,242,242);

  .router-link-active {
    font-size: 25px;
    color: #409EFF;
    text-decoration: none;
  }

  .user-info {
    display: flex;
    align-items: center;
    height: 100%;

    img {
      margin-right: 20px;
    }
  }
}

.el-main {
  padding: 0;
}
</style>
