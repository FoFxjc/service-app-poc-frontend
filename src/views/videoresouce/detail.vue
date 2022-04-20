<template>
  <div class="dashboard-container">
    <el-row :gutter="10">
      <el-col :span="6">
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            Resource Data
          </p>
          <el-divider></el-divider>
          <div
            style="
              padding: 0px 10px 10px 10px;
              margin-top: -15px;
              height: 200px;
            "
          ></div>
        </el-card>
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            User Data
          </p>
          <el-divider></el-divider>
          <div
            style="
              padding: 0px 10px 10px 10px;
              margin-top: -15px;
              height: 200px;
            "
          ></div>
        </el-card>
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            Action logs
          </p>
          <el-divider></el-divider>
          <div style="padding: 0px 10px 10px 10px; margin-top: -15px">
            <el-table :data="tableData" style="font-size: 12px">
              <el-table-column prop="date" label="Datetime"> </el-table-column>
              <el-table-column prop="name" label="User" width="90">
              </el-table-column>
              <el-table-column prop="address" label="Action" width="120">
              </el-table-column>
            </el-table>
          </div>
        </el-card>
      </el-col>
      <el-col :span="18">
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            Shooting Datetime
          </p>
          <el-divider></el-divider>
          <div
            style="
              padding: 0px 10px 10px 10px;
              margin-top: -15px;
              height: 200px;
            "
          ></div>
        </el-card>
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            Video/Picture List
          </p>
          <el-divider></el-divider>
          <div
            style="
              padding: 0px 10px 10px 10px;
              margin-top: -15px;
              height: 500px;
            "
          ></div>
        </el-card>
        <el-card class="box-card" :body-style="{ padding: '5px 0px 10px 0px' }">
          <p
            style="
              margin-bottom: -10px;
              margin-left: 15px;
              margin-right: 15px;
              font-size: 16px;
            "
          >
            Cost Bill
          </p>
          <el-divider></el-divider>
          <div
            style="
              padding: 0px 10px 10px 10px;
              margin-top: -15px;
              height: 200px;
            "
          ></div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import LineChart from "./components/LineChart";
import BarChart from "./components/BarChart";
const lineChartData = {
  newVisitis: {
    expectedData: [
      3000, 3000, 3000, 3000, 6000, 3000, 3000, 3000, 3000, 4500, 4500, 3000,
    ],
    actualData: [120, 82, 91, 154, 162, 140, 145],
  },
  messages: {
    expectedData: [200, 192, 120, 144, 160, 130, 140],
    actualData: [180, 160, 151, 106, 145, 150, 130],
  },
  purchases: {
    expectedData: [80, 100, 121, 104, 105, 90, 100],
    actualData: [120, 90, 100, 138, 142, 130, 130],
  },
  shoppings: {
    expectedData: [130, 140, 141, 142, 145, 150, 160],
    actualData: [120, 82, 91, 154, 162, 140, 130],
  },
};

export default {
  name: "Dashboard",
  computed: {
    ...mapGetters(["name"]),
  },
  components: {
    LineChart,
    BarChart,
  },
  data() {
    return {
      tableData: [
        {
          date: "2022-03-31 11:22:33",
          name: "Admin01",
          address: "Created",
        },
        {
          date: "2022-04-02 11:22:33",
          name: "Admin01",
          address: "Changed Price",
        },
        {
          date: "2022-04-10 11:22:33",
          name: "Admin02",
          address: "Published",
        },
      ],
      lineChartData: lineChartData.newVisitis,
      viewdownload_Data: [
        {
          date: "2016-05-03",
          name: "User001",
          province: "",
          city: "View",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-02",
          name: "User101",
          province: "",
          city: "View",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-04",
          name: "User401",
          province: "",
          city: "View",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-01",
          name: "User301",
          province: "¥ 4500",
          city: "Download",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-08",
          name: "User201",
          province: "¥ 4500",
          city: "Download",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-06",
          name: "User101",
          province: "¥ 3000",
          city: "Download",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-07",
          name: "User011",
          province: "¥ 3000",
          city: "Download",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
      ],
    };
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
.data_field {
  margin-top: 50px;

  .data_field_label {
    font-size: 12px;
    line-height: 0px;
    color: #999;
    margin-bottom: -5px;
  }
  .data_field_content {
    font-size: 14px;
    font-weight: normal;
  }
}

.bottom {
  margin-top: -20px;
  padding: 0px 15px 0px 20px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
</style>
