<script setup lang="ts">
const props = defineProps<{
  provider: 'google' | 'naver' | 'kakao'
  label: string
}>()

const emit = defineEmits<{
  (e: 'click'): void
}>()

const handleClick = () => {
  emit('click')
}
</script>

<template>
  <button
    type="button"
    class="social-btn"
    :class="provider"
    @click="handleClick"
  >
    <span class="icon">
      <!-- 여기서는 간단히 이니셜만, 원하면 이미지로 교체 -->
      <span v-if="provider === 'google'">G</span>
      <span v-else-if="provider === 'naver'">N</span>
      <span v-else>K</span>
    </span>
    <span class="label">{{ label }}</span>
  </button>
</template>

<style scoped>
.social-btn {
  width: 100%;
  height: 44px;
  border-radius: 8px;
  border: 1px solid transparent;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  font-size: 14px;
  cursor: pointer;
  font-weight: 500;
}

/* 공통 아이콘 박스 */
.icon {
  width: 22px;
  height: 22px;
  border-radius: 4px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
}

/* 개별 스타일 */
.social-btn.google {
  background: #ffffff;
  border-color: #dadce0;
  color: #202124;
}
.social-btn.google .icon {
  background: #ffffff;
  border: 1px solid #dadce0;
}

.social-btn.naver {
  background: #03c75a;
  color: #ffffff;
}
.social-btn.naver .icon {
  background: #ffffff;
  color: #03c75a;
}

.social-btn.kakao {
  background: #fee500;
  color: #381e1f;
}
.social-btn.kakao .icon {
  background: #381e1f;
  color: #fee500;
}

.label {
  flex: 1;
  text-align: center;
}
</style>
