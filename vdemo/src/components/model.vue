<script setup>

// 消息管理页面
import { NButton, NTable, NSpace, NIcon } from "naive-ui";
</script>

<template>
  <div class="build">
    <div >
      <n-button> 新建 </n-button>
    </div>
  
    <div>
      <n-table :single-line="false">
        <div class="mes_box">
          <thead >
            <tr>
              <th>模板ID</th>
              <th>模板名称</th>
              <th>消息标题</th>
              <th>消息正文</th>
              <th>标题变量</th>
              <th>正文变量</th>
              <th>效果图示</th>
              <th>操作</th>
            </tr>
          </thead>
          <tbody class="fcenter">
            <tr>
              <td>放弃</td>
              <td>反常的</td>
              <td>彻底废除</td>
              <td>...</td>
              <td>干！我刚才背的是啥</td>
              <td>干！我刚才背的是啥</td>
              <td>干！我刚才背的是啥</td>
              <td>
                <n-button>
                  <n-icon @click="change">
                    <pic-icon />
                  </n-icon>
                </n-button>
                <n-button>
                  <n-icon>
                    <edit-icon />
                  </n-icon>
                </n-button>
                <n-button>
                  <n-icon>
                    <del-icon color="red" />
                  </n-icon>
                </n-button>
              </td>
            </tr>
          </tbody>
        </div>
      </n-table>
    </div>
  

  </div>

</template>

<script>
import { PictureOutlined as PicIcon } from "@vicons/antd";
import { DeleteOutlined as DelIcon } from "@vicons/antd";
import { EditOutlined as EditIcon } from "@vicons/antd";

export default {
  name: "Home",
  components: {
    PicIcon,
    DelIcon,
    EditIcon,
  },
  methods: {
    // 修改图片
    change(){


    }
  },
};
</script>
<style scoped>
.fcenter tr{
  height: 300px;
}

td{
  width: 12.5%;
}
.build{
  margin-top: 25px;
  margin-left: 25px;

}
</style>
