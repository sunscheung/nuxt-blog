<template>
  <Menu active-name="admin" :open-names="['1','2','3']" class="menu-left" @on-select="getIndex" style="width:100%;min-height:100vh;">
    <Submenu name="1">
        <template slot="title">
            <Icon class="iconfont icon-xitong"></Icon>
            控制面板
        </template>
        <MenuItem name="admin"><Icon class="iconfont icon-zichangailan"></Icon>系统概览</MenuItem>
        <MenuItem name="article"><Icon class="iconfont icon-navicon-wzgl"></Icon>发布文章</MenuItem>
        <MenuItem name="articleList"><Icon class="iconfont icon-wenzhangliebiaoxiangqing"></Icon>文章列表</MenuItem>
    </Submenu>
    <Submenu name="2">
        <template slot="title">
            <Icon class="iconfont icon-banbengengxin1"></Icon>
            版本控制
        </template>
        <MenuItem name="version"><Icon class="iconfont icon-fabu"></Icon>发布版本</MenuItem>
    </Submenu>
    <Submenu name="3">
      <template slot="title">
        <Icon class="iconfont icon-pinglun1"></Icon>
        评论管理
      </template>
      <MenuItem name="comment"><Icon class="iconfont icon-pinglun"></Icon>评论列表</MenuItem>
    </Submenu>
  </Menu>
</template>
<script>
export default {
  methods: {
    getIndex (val) {
      this.$router.push({name: val})
    }
  }
}
</script>
<style lang="less">
.ivu-menu-item {
  font-weight: bold !important;
  i {
    font-weight: bold;
  }
}
.iconfont {
  font-weight: bold;
}
</style>
