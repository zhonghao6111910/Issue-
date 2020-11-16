<template>
  <div>
    <h1 style="color:blue">GBA Issue管理系统</h1>
    <div id="HeaderMe">
      <el-button type="primary" round>注销</el-button>
      <el-button type="primary" round>登陆</el-button>
      <span>
        <el-alert title="成功提示的文案" type="success" show-icon></el-alert>
      </span>
      <el-button type="primary" round>修改个人信息</el-button>
    </div>
    <div id="HeaderMenu">
      <el-button type="primary" round>创建新Issue</el-button>
      <el-button type="primary" round>Issue报表</el-button>
      <el-button type="primary" round>账号管理</el-button>
    </div>
  </div>
</template>
<style>
#HeaderMe > * {
  float: left;
}
#HeaderMenu {
  width: 100%;
  height: 35px;
  float: left;
}
</style>
