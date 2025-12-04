<script setup lang="ts">
import SocialLoginButton from './SocialLoginButton.vue'

const handleClick = () => {
  // TODO: 카카오 로그인 SDK / redirect
  console.log('Kakao login clicked')
}
</script>

<template>
  <SocialLoginButton
    provider="kakao"
    label="카카오로 계속"
    @click="handleClick"
  />
</template>
