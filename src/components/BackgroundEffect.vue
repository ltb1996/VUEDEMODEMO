<template>
  <div class="background-wrapper">
    <!-- CSS 渐变背景层 -->
    <div class="gradient-overlay">
      <div class="gradient-inner"></div>
    </div>

    <!-- UnicornStudio 动态背景 -->
    <div class="aura-background-component">
      <div class="aura-inner">
        <div
          ref="unicornContainer"
          data-us-project="BqS5vTHVEpn6NiF0g8iJ"
          class="unicorn-container"
        ></div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

const unicornContainer = ref(null);

onMounted(() => {
  // 等待 UnicornStudio 加载完成后初始化
  const initUnicorn = () => {
    if (window.UnicornStudio) {
      if (!window.UnicornStudio.isInitialized) {
        try {
          window.UnicornStudio.init();
          window.UnicornStudio.isInitialized = true;
          console.log("UnicornStudio initialized successfully");
        } catch (error) {
          console.error("UnicornStudio init error:", error);
        }
      } else {
        // 如果已经初始化，尝试重新初始化当前容器
        try {
          window.UnicornStudio.init();
          console.log("UnicornStudio re-initialized");
        } catch (error) {
          console.error("UnicornStudio re-init error:", error);
        }
      }
    } else {
      // 如果还没加载，等待后重试
      console.log("Waiting for UnicornStudio to load...");
      setTimeout(initUnicorn, 100);
    }
  };

  // 延迟初始化，确保 DOM 完全渲染
  setTimeout(initUnicorn, 0);
});
</script>

<style scoped>
.background-wrapper {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  pointer-events: none;
  z-index: 0;
}

.gradient-overlay {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.gradient-inner {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  /* background: linear-gradient(to bottom,
      rgba(88, 28, 135, 0.2) 0%,
      rgba(0, 0, 0, 1) 50%,
      rgba(0, 0, 0, 1) 100%); */
  background: rgba(0, 0, 0, 1);
}

.aura-background-component {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 1100px;
  z-index: 1;
}

.aura-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.unicorn-container {
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
}
</style>
