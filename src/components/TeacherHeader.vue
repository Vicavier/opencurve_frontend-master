<template>
  <div>
    <div class="header">
      <div class="logo">
        <router-link to="/">OpenCurve</router-link>
      </div>
      <!-- 水平一级菜单 -->
      <div style="float: left;">
        <el-menu
            mode="horizontal"
            :ellipsis="false"
            text-color="#000000"
            active-text-color="#3989fa">
          <el-menu-item index="1">
            <router-link to="/TeacherMain">主页</router-link>
          </el-menu-item>
          <el-menu-item index="2">
            <router-link to="/TeacherCourseCenter">课程中心</router-link>
          </el-menu-item>
          <el-menu-item index="3">
            <router-link to="/TeacherNotificationCenter">通知中心</router-link>
          </el-menu-item>
          <el-menu-item index="4">
            <router-link to="/TeacherAssignmentCenter">作业中心</router-link>
          </el-menu-item>
          <el-menu-item index="5">
            <router-link to="/">个人中心</router-link>
          </el-menu-item>
        </el-menu>
      </div>

      <div class="header-right">
        <div class="header-user-space">
          <!-- 用户头像 -->
          <div class="user-avatar">
            <img src="../assets/logo.png">
          </div>
          <!-- 用户名下拉菜单 -->
          <el-dropdown class="user-name" trigger="click">
            <span class="el-dropdown-link"> user <i class="el-icon-caret-bottom"></i></span>
            <template #dropdown>
              <el-dropdown-menu>
                <el-dropdown-item>个人资料</el-dropdown-item>
                <el-dropdown-item>修改密码</el-dropdown-item>
                <el-dropdown-item>退出登录</el-dropdown-item>
                <!--                <el-dropdown-item disabled>Action 4</el-dropdown-item>-->
                <!--                <el-dropdown-item divided>Action 5</el-dropdown-item>-->
              </el-dropdown-menu>
            </template>
          </el-dropdown>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeacherHeader"
}
</script>

<style scoped>
.header {
  position: relative;
  box-sizing: border-box;
  width: 100%;
  height: 70px;
  font-size: 22px;
}

.header .logo {
  float: left;
  margin-left: 60px;
  margin-top: 17px;
  height: 29px;
  width: 160px;
  vertical-align: middle;
}


/* --------------- 水平一级菜单栏的样式--------------------- */
.el-menu.el-menu--horizontal {

  float: left;
  margin-left: 50px;
  background: transparent;
}

.el-menu--horizontal > .el-menu-item.is-active {
  /* border-bottom: 2px solid #3989fa;
  color: #3989fa; */
  font-weight: bold;
}

.el-menu--horizontal > .el-menu-item {
  font-size: 16px;
  margin: 0 15px;
}

/* --------------- 用户头像区域的样式 ---------------- */
.header-right {
  float: right;
  padding-right: 50px;
}

.header-user-space {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 70px;
}

.user-avatar {
  margin-left: 20px;
}

.user-avatar img {
  display: block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
}
</style>