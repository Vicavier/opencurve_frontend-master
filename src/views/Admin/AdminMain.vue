<template>
  <div class="bg">
    <div class="adminMain">
      <p>Administrator Main</p>
    </div>
    
  </div>
</template>

<script>
import AdminHeader from "@/components/AdminHeader";
export default {
  name: "AdminMain",
  components: {AdminHeader}
}
</script>

<style scoped>
.bg {
  background-color: rgb(243,244,246);
}
.adminMain{
  width:80%;
  margin:0 auto;
  background-color: rgb(243,244,246);
}
</style>