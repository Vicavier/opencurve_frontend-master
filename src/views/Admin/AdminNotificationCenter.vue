<template>
  <div class="bg">
    <div class="notification-admin">
      <el-main>
        <p>Notification Center</p>

        <el-table :data="notifications">
          <el-table-column label="Course" prop="course"></el-table-column>
          <el-table-column label="Title" prop="title"></el-table-column>
          <el-table-column label="Sender" prop="sender"></el-table-column>
          <el-table-column label="Last Edit Time" prop="time"></el-table-column>
        </el-table>
      </el-main>
    </div>
      
  </div>
</template>

<script>
import AdminHeader from "@/components/AdminHeader";
export default {
  name: "AdminNotificationCenter",
  components: {AdminHeader},

  data() {
    return {
      notifications: [
        {
          title: 'Notification 1',
          sender: 'AAAAA',
          time: '2022/09/01',
          course: 'Course 1'
        },
        {
          title: 'Notification 2',
          sender: 'BBBBBB',
          time: '2022/09/30',
          course: 'Course 2'
        },
        {
          title: 'Notification 3',
          sender: 'CCCCC',
          time: '2022/10/15',
          course: 'Course 3'
        }
      ]
    }
  }
}
</script>

<style scoped>
.bg {
  background-color: rgb(243,244,246);
}
.notification-admin{
  width:80%;
  margin:0 auto;
  background-color: rgb(243,244,246);
}
</style>