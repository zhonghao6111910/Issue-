<template>
  <div>
    <!-- //Issue题目 -->
    <div style=" margin-top:10px"></div>
    <h1>Issue题目</h1>
    <div style="margin: 20px 0;"></div>
    <el-input
      type="textarea"
      :autosize="{ minRows: 2, maxRows: 4 }"
      placeholder="请输入内容"
      v-model="textarea"
      maxlength="80"
      show-word-limit
    >
    </el-input>

    <h5>基本信息</h5>
    <hr style="border-style:dashed" />
    <div id="BasicInfo">
      <!-- //Issue NO -->
      <el-col :span="4">
        Issue NO
        <el-input placeholder="系统自动生成" v-model="input" :disabled="true">
        </el-input>
      </el-col>
      <!-- 创建时间 -->
      <el-col :span="4">
        创建时间
        <el-input placeholder="系统自动生成" v-model="input" :disabled="true">
        </el-input>
      </el-col>
      <!--    Issue 类型 -->
      <el-col :span="4">
        Issue 类型
        <el-input type="text" v-model="text" maxlength="30" show-word-limit>
        </el-input>
      </el-col>
      <!-- Issue等级 -->
      <el-col :span="4">
        Issue等级
        <el-select v-model="value" placeholder="内容">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          >
          </el-option>
        </el-select>
      </el-col>

      <!-- 影响版本 -->
      <el-col :span="4">
        影响版本
        <el-input type="text" v-model="text" maxlength="30" show-word-limit>
        </el-input>
      </el-col>
      <!-- 计划修改时间 -->
      <div class="block">
        <el-col :span="8">
          计划修改时间
          <el-date-picker
            v-model="value2"
            align="right"
            type="date"
            placeholder="选择日期"
            :picker-options="pickerOptions"
          >
          </el-date-picker>
        </el-col>
      </div>
      <!-- 实际完成时间 -->
      <el-col :span="4">
        实际完成时间
        <el-input placeholder="系统自动生成" v-model="input" :disabled="true">
        </el-input>
      </el-col>
    </div>
    <div id="box2">
      <el-col :span="8">
        重现步骤
      </el-col>

      <el-input
        type="textarea"
        v-model="textarea"
        :autosize="{ minRows: 4 }"
        maxlength="2000"
        show-word-limit
      >
      </el-input>

      <el-col :span="5">
        指派修改人
        <el-input type="text" v-model="text" maxlength="30" show-word-limit>
        </el-input>
      </el-col>
      <el-button type="primary" round id="button1">提交</el-button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      input: "",
      text: "",
      formInline: {
        user: "",
        region: ""
      },
      //计划修改时间
      pickerOptions: {
        disabledDate(time) {
          return time.getTime() < Date.now();
        }
      },
      value1: "",
      value2: "",

      //issue等级
      options: [
        {
          value: "选项1",
          label: "最高"
        },
        {
          value: "选项2",
          label: "较高"
        },
        {
          value: "选项3",
          label: "一般"
        },
        {
          value: "选项4",
          label: "低"
        }
      ],
      value: "",
      text: "",
      textarea: ""
    };
  }
};
</script>

<style>
#form1 {
}
#BasicInfo {
  width: 100%;
  height: 180px;
}
#BasicInfo > * {
  float: left;
  margin-left: 5%;
}
#box2 > * {
  float: inherit;
  margin-top: 10px;
  margin-left: 20px;
}
#button1 {
  margin-left: 45%;
}
</style>
