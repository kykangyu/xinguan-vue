<template>
  <el-container class="main_container">
    <el-header>
      <div class="left_box">
        <img src="..\assets\img\timg.gif" />
        <span>新冠物资管理系统</span>
      </div>

      <div class="right_box">
        <el-dropdown>
          <img src="..\assets\img\timg.gif" />
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item icon="el-icon-house">系统首页</el-dropdown-item>
            <el-dropdown-item icon="el-icon-ship">交流讨论</el-dropdown-item>
            <el-dropdown-item icon="el-icon-switch-button">退出登录</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </el-header>

    <el-container>
      <el-aside width="200px">
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#001529"
          text-color="#fff"
          active-text-color="#ffd04b"
        >
          
        </el-menu>
      </el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style lang="less" scoped>
.main_container {
  height: 100%;
}

.el-header {
  background-color: #001529;
  display: flex;
  justify-content: space-between;
  padding-left: 0;
  color: #ffffff;
  align-items: center;
  font-size: 20px;

  /*左边logo和标题*/

  .left_box {
    display: flex;
    align-items: center;

    /*logo*/

    img {
      width: 60px;
      height: 60px;
      margin: 0px 0px 10px 15px;
    }

    /*标题*/

    span {
      margin-left: 15px;
    }
  }

  /*右边的登录头像*/

  .right_box {
    .el-dropdown > img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background-color: #ffffff;
      margin: 0px 15px 0px 0px;
      background-size: contain;
    }
  }
}

.el-aside {
  background-color: #001529;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

// 下拉菜单
// .el-dropdown-link {
//   cursor: pointer;
//   color: #409eff;
// }
// .el-icon-arrow-down {
//   font-size: 12px;
// }
</style>
