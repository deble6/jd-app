<template>
  <div>
    <el-container>
      <el-header height="50px">

        <div class="user-info">
          <span class="iconfont iconzuojiantou" @click="back" v-show="meta.goBackShow"></span>
          <span
            v-for="(item, index) in titleList"
            :key="index"
            @click="toPage(item)"
            :class="{active: item.active }">
            {{item.titleName}}
          </span>
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
  computed: {
    titleList () {
      return this.$route.meta.title
    },
    goBackBtn () {
      return this.$route.meta.goBack
    },
    meta () {
      return this.$route.meta
    }
  },
  methods: {
    back () {
      this.$router.push({path: this.goBackBtn})
    },
    toPage (data) {
      if (data.toPath !== this.$route.path) {
        this.$router.push({path: data.toPath})
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
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50px;
    font-size: 20px;
    width: 100%;

    .iconzuojiantou {
      position: absolute;
      top: 50%;
      left: 10px;
      transform: translate(0, -50%);
    }

    span {
      margin: 0 10px;
    }

    .active {
      color: #C39862;
    }
  }
}

.el-main {
  padding: 0;
}
</style>
