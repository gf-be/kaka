<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { NSpace, NLayout, NLayoutHeader, NLayoutContent, NLayoutFooter } from "naive-ui";

import left from "./components/left.vue";
import right from "./components/right.vue";
import model from "./components/model.vue";
</script>

<template>

<!-- 有个bug 没有完全实现视频里的效果。点击的模块都会亮起，视频里是点哪个哪个亮 -->
  <div class="box">
    <div>
      <div class="view">
        <div class="left">
          <div>
            <button :class="onMes ? 'active' : 'priva'" @click="changeMes">消息管理</button>

            <button :class="onMod ? 'active' : 'priva'" @click="changeMod">模块管理</button>
          </div>
        </div>

        <div class="right">
          <right :isFir="isFirst" :mes=onMes :mod=onMod @fn="closeMes" @fn1="closeMod" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      onMod: false,
      onMes: false,
      isFirst:""
    };
  },
  methods: {
    changeMes() {
      this.onMes = !this.onMes;
      this.isFirst = "mes"
      console.log(this.onMes);
      
    },
    changeMod() {
      this.onMod = !this.onMod;
      this.isFirst = "mod"
      
      console.log(this.onMod);

    },
    closeMes(){
      
      this.onMes = !this.onMes;
    },
    closeMod(){
      
      this.onMod = !this.onMod;
    }
  },
};
</script>
<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

* {
  margin: o;
  padding: 0;
}
.view {
  display: flex;
  justify-content: center;
}

.left {
  width: 160px;
  height: 38.1875rem;
  background: #001323;

  /* float: left; */
}

.right {
  width: 1051px;
  height: 611px;
}
.active {
  background: #2781ee;
  width: 9.5rem;
  height: 2.3125rem;
  color: white;
}

.left_box {
  height: 38.1875rem;
  width: 9.875rem;
}
.priva {
  width: 9.5rem;
  height: 2.3125rem;
  color: white;
  background: #001323;
}
</style>
