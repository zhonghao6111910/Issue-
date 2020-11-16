<template>
  <div>
    Issue查询
    <hr style="border-style:dashed" />
    <el-col :span="4">
      Issue NO
      <el-input type="text" v-model="text" maxlength="30" show-word-limit>
      </el-input>
    </el-col>

    Isuee状态
    <el-select v-model="value" placeholder="请选择">
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value"
      >
      </el-option>
    </el-select>

    <el-col :span="4">
      创建人
      <el-input type="text" v-model="text" maxlength="30" show-word-limit>
      </el-input>
    </el-col>

    <el-col :span="4">
      修改人
      <el-input type="text" v-model="text" maxlength="30" show-word-limit>
      </el-input>
    </el-col>
    创建时间 修改时间
  </div>
</template>
<script>
export default {
  data() {
    return {
      options: [
        {
          value: "选项1",
          label: "待修改"
        },
        {
          value: "选项2",
          label: "待验证"
        },
        {
          value: "选项3",
          label: "已关闭"
        }
      ],
      value: "",
      text: "",
      textarea: ""
    };
  }
};
</script>
