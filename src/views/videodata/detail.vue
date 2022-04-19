<template>
  <div class="dashboard-container">
    <el-row :gutter="10">
      <el-col :span="20">
        <el-card class="box-card">
          <el-row :gutter="10">
            <el-col :span="4">
              <img
                style="width: 100%; height: 100%"
                src="https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3"
              />
            </el-col>
            <el-col :span="16"
              ><el-descriptions title="Video Title">
                <el-descriptions-item label="Video ID"
                  >18100000000</el-descriptions-item
                >
                <el-descriptions-item label="Create Date"
                  >18100000000</el-descriptions-item
                >
                <el-descriptions-item label="Create User"
                  >18100000000</el-descriptions-item
                >
                <el-descriptions-item label="Status"
                  >18100000000</el-descriptions-item
                >
              </el-descriptions>
            </el-col>
          </el-row>
        </el-card>
      </el-col>
      <el-col :span="4">
        <el-card class="box-card"> 价格信息 </el-card>
      </el-col>
    </el-row>
    <el-row :gutter="10">
      <el-col :span="6">
        <el-card class="box-card" style="height: 300px">
          预约/定时信息
        </el-card>
        <el-card class="box-card" style="height: 300px"> 摄影信息 </el-card>
        <el-card class="box-card" style="height: 300px"> 卫星信息 </el-card>
      </el-col>
      <el-col :span="18">
        <el-card class="box-card" style="height: 700px"> 下载信息 </el-card>
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
