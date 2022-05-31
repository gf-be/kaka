<script setup>
import { defineComponent, ref } from "vue";
import { NButton, NTable, NSpace, NSelect, NIcon, NForm } from "naive-ui";
</script>

<template>
  <div class="box">
    <div class="left">
      <div class="content">
        <n-button type="primary">新建消息分组</n-button>
      </div>
    </div>

    <div class="right">
      <div class="newMes">
        <p>新建消息</p>
      </div>
      <form action="" class="mesForm">
        <tr>
          <td>
            <p>消息名称</p>
          <n-select show-arrow="false"  size="small" placeholder="请输入" />  </td>
        </tr>
        <tr>
          <td>
            <p>所属消息分组</p>
            <n-select  size="small" placeholder="" />
          </td>
        </tr>
        <tr>
          <td>
            <p>消息工具</p>
            <n-select placeholder="请选择" size="small" />
          </td>
        </tr>
        <tr>
          <td>
            <p>消息类型</p>
            <n-select placeholder="请选择" size="small" />
          </td>
        </tr>
        <tr>
          <td>
            <p>选择模板</p>
            <n-select placeholder="请选择" size="small" />
          </td>
        </tr>
      </form>
    </div>
  </div>
</template>

<style scoped>
.box {
  background: #f4f6f8;
  position: relative;
  height: 571px;
}
.left {
  width: 37%;
  left: 0;
  height: 200px;
  position: absolute;
  margin-left: 10px;
  background-color: white;
}

.right {
  width: 60%;
  right: 0;
  height: 400px;
  background-color: white;
  position: absolute;
}

.content {
  margin-left: 20px;
  margin-top: 20px;
}

.newMes {
  margin-left: 50px;
  margin-top: 20px;
}

td {
  display: flex;
  width: 400px;
}
.mesForm tr td p{
  width: 170px;
  margin-left: 30px;
}
</style>
