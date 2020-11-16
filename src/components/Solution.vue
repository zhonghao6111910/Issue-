<template>
  <div>
    <h1>解决方案</h1>
    <div style="margin: 20px 0;"></div>
    <el-input
      type="textarea"
      :autosize="{ minRows: 2 }"
      placeholder="请输入内容"
      v-model="textarea"
    >
    </el-input>
    <el-button type="primary" round id="button1">提交</el-button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      textarea: ""
    };
  }
};
</script>
<style>
#button1 {
  margin-top: 20px;
  margin-left: 45%;
}
</style>
