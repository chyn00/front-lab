<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <!-- 그냥 라우터 뷰만 렌더링 -->
  <RouterView />
</template>

<style>
/* 선택: 전역 기본 스타일만 간단히 두고 싶으면 여기서 정의 */
body {
  margin: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI',
  sans-serif;
}
</style>
