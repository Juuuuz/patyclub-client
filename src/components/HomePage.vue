<template>
  <div class="common-layout">
    <el-container>
      <el-header>
        <button class="btns">所有活動</button>
        <button class="btns">創建活動</button>
        <button class="btns" @click="bShowModal = true" style="margin-right:30px">登入</button>
      </el-header>
      <el-main class="note" :style="note"></el-main>
      <el-footer>Footer</el-footer>
      <LoginModal :openModal="bShowModal" @close-modal="bShowModal = false" />
    </el-container>
    <!-- <main id="Home" class="note" :style="note">
    <div class="main-bar">
      <button class="btns">所有活動</button>
      <button class="btns">創建活動</button>
      <button class="btns" @click="bShowModal = true">登入</button>
    </div>
    <LoginModal :openModal="bShowModal" @close-modal="bShowModal = false" />
  </main> -->
  </div>
</template>

<script>
import LoginModal from "./LoginModal.vue";
export default {
  components: {
    LoginModal,
  },
  data() {
    return {
      bShowModal: false,
      note: {
        backgroundImage:
          "url(" + require("../assets/backgroundImage.png") + ")",
        backgroundSize: "100%",
      },
    };
  },
  methods: {
    routeLoginPage() {},
  },
};
</script>
<style>
.el-header {
  background-color: #b3c0d1;
  color: var(--el-text-color-primary);
  text-align: right;
  line-height: 60px;
}
.el-footer {
  background-color: #b3c0d1;
  color: var(--el-text-color-primary);
  text-align: center;
  line-height: 52px;
}

.el-aside {
  background-color: #d3dce6;
  color: var(--el-text-color-primary);
  text-align: center;
  line-height: 200px;
}

.el-main {
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
