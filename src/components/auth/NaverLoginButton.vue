<script setup lang="ts">
import SocialLoginButton from './SocialLoginButton.vue'

const handleClick = () => {
  // TODO: 네이버 로그인 SDK / redirect
  console.log('Naver login clicked')
}
</script>

<template>
  <SocialLoginButton
    provider="naver"
    label="네이버로 계속"
    @click="handleClick"
  />
</template>
