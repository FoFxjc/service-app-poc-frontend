<template>
  <div class="dashboard-container">
    <el-row :gutter="10">
      <el-col :span="24">
        <el-card class="box-card"> 视频信息 </el-card>
      </el-col>
    </el-row>
    <el-row :gutter="10">
      <el-col :span="8">
        <el-card class="box-card" style="height: 300px"> 视频文件 </el-card>
        <el-card class="box-card" style="height: 300px"> 工具栏 </el-card>
      </el-col>
      <el-col :span="16">
        <el-card class="box-card" style="height: 400px"> 视频编辑器 </el-card>
        <el-card class="box-card" style="height: 300px"> 时间轴 </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "Dashboard",
  computed: {
    ...mapGetters(["name"]),
  },
};
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
    font-weight: 100;
  }
}
.box-card {
  margin-bottom: 20px;
  font-size: 20px;
  font-weight: bold;
  &-text {
    font-size: 18px;
    line-height: 46px;
    font-weight: normal;
  }
}
</style>
