<script setup lang="ts">
import GoogleLoginButton from '@/components/auth/GoogleLoginButton.vue'
import NaverLoginButton from '@/components/auth/NaverLoginButton.vue'
import KakaoLoginButton from '@/components/auth/KakaoLoginButton.vue'
</script>

<template>
  <main class="login-page">
    <section class="login-card">
      <h1 class="login-title">로그인</h1>
      <p class="login-subtitle">소셜 계정으로 빠르게 시작하세요</p>

      <div class="login-buttons">
        <GoogleLoginButton />
        <NaverLoginButton />
        <KakaoLoginButton />
      </div>
    </section>
  </main>
</template>

<style scoped>
.login-page {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f7;
}

.login-card {
  width: 360px;
  padding: 32px 28px;
  border-radius: 16px;
  background: #ffffff;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.06);
  text-align: center;
}

.login-title {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 8px;
}

.login-subtitle {
  font-size: 13px;
  color: #666;
  margin-bottom: 24px;
}

.login-buttons {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
</style>
