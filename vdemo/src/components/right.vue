<script setup>
// 设置公共模块，点击功能发生跳转，展示不同页面
//

// 有个bug  孩子不会了。先点击模板管理，再点击消息管理，然后点关闭消息管理，模板管理不会显示
import model from "./model.vue"
import message from "./message.vue"
import {
  NSpace,
  NLayout,
  NLayoutHeader,
  NLayoutContent,
  NLayoutFooter,
  NButton,
  NTag,
  NDynamicTags
} from "naive-ui";
</script>


<template>
  <footer class="top">
    <n-tag closable size="large"  @close="mesClose" v-show="mes"> 消息管理 </n-tag>
    <n-tag closable  size="large" @close="modClose" v-show="mod"> 模板管理 </n-tag>

  </footer>
  <section>
    <!-- 不同模块 -->

    <div class="center">
      <div v-show="mod" >

      <model v-if="mod && isFir == 'mod' " />
      </div>
      <div v-show="mes" >
        
        <message v-show="mes && isFir == 'mes' " />
      </div>
    </div>
  </section>
</template>

<script>


export default {
  components: { message },
  props:{
    mes: Boolean,
    mod: Boolean,
    isFir:String
  },
  methods: {
    mesClose(){
      this.$emit("fn")
    },
    modClose(){
      this.$emit("fn1")
    }
  }

}
</script>
<style scoped>
.top {
  width: 1051px;
  height: 40px;
  background: #f4f6f8;
}

.center {
  margin: 0 auto;
}
</style>
