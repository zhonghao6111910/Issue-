<template>
  <div>
    <div style="margin: 20px 0;"></div>
    <h4>查询条件</h4>
    <hr style="border-style:dashed" />
    <el-col :span="4">
      用户ID：
      <el-input type="text" v-model="text"> </el-input>
    </el-col>
    <el-col :span="4">
      用户姓名：
      <el-input type="text" v-model="text"> </el-input>
    </el-col>
    <div>
      <el-button type="primary" round id="button1">查询</el-button>
      <el-button type="primary" round id="button1">清空</el-button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      text: ""
    };
  }
};
</script>
