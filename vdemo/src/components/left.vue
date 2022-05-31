<script setup>
// 本来想将页面分为左和右，在进行点击发生页面改变功能时，发现难以实现，决定将这一部分转到 app.vue  
// 因此，本文件无用处

// 
import { ref } from "vue";
import {
  NSpace,
  NLayout,
  NLayoutHeader,
  NLayoutContent,
  NLayoutFooter,
  NButton,
} from "naive-ui";
</script>



<template>
  <div class="left_box">
    <button quaternary class="left_aa" :class=" onMes ? active : ''" @click="changeMes"> 消息管理 </button>
  
    <button quaternary class="left_aa" :class=" onMod ? active : ''" @click="changeMod"> 模块管理 </button>
  </div>
</template>
<script>
export default {
  data() {
    return {
    onMod:false,
    onMes: false,
    active:'active',
    }
  },
  methods: {
    changeMes(){
      this.onMes = !this.onMes
      this.$emit('fn')
    },
    changeMod(){
      this.onMod = !this.onMod
    }
  },
};
</script>
<style scoped>
.word {
  color: white;
  background: #001323;
}
.active {
  background: #2781ee;
}

.left_box {
  height: 38.1875rem;
  width: 9.875rem;
}
.left_aa {
  width: 9.5rem;
  height: 2.3125rem;
}
</style>
