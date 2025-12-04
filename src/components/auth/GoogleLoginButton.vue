<script setup lang="ts">
import SocialLoginButton from './SocialLoginButton.vue'

const handleClick = () => {
  // TODO: 여기서 구글 로그인 SDK or 백엔드 OAuth 엔드포인트로 redirect
  // 예: window.location.href = '/oauth2/authorization/google'
  console.log('Google login clicked')
}
</script>

<template>
  <SocialLoginButton
    provider="google"
    label="Google 계정으로 계속"
    @click="handleClick"
  />
</template>
