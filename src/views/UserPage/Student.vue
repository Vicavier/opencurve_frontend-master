<template>
  <div id="studentpage">
    <div class="activity">
      <div @click="toInfo()" tabindex="1">个人资料</div>
      <div @click="toSetting()" tabindex="2">账号设置</div>
      <div @click="toHistory()" tabindex="3">浏览历史</div>
      <div @click="toVip()" tabindex="4">会员中心</div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
    components: {
        
  },
  methods: {
    toInfo(){
      this.$router.push({
        path: '/userPage/StudentSelfCenter/information',
      })
    },
    toSetting(){
      this.$router.push({
        path: '/userPage/StudentSelfCenter/setting',
      })
    },
    toHistory(){
      this.$router.push({
        path: '/userPage/StudentSelfCenter/history',
      })
    },
    toVip(){
      this.$router.push({
        path: '/userPage/StudentSelfCenter/vip',
      })
    },
      
  },
  mounted() {
    this.$router.push({
      path: '/userPage/StudentSelfCenter/information',
    })
}
}
</script>

<style scoped>
  @import '../../lib/userpage_video_nav.css'
</style>