<template>
  <div class="container">
    <div class="title">
      <h2>{{title1}}</h2>
      <NuxtLink to="/students">生徒の情報を見る</NuxtLink>
    </div>
    <div class="title">
      <h2>{{title2}}</h2>
      <NuxtLink to="/management">管理画面を見る</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title1: '生徒一覧',
      title2: '管理者',
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title {
  margin: 20px;
}
</style>