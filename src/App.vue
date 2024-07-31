<script setup>
  let message = 'Hello World';
  const link = 'https://google.com';
  // const isActive = true;
  // const isBlack = true;
  const activeColor = 'red';
  const fontStress = '900';
  const styleObjcet = {
    color: 'red',
    fontWeight: 900,
  };

  const upperCase = () =>{
    message = message.toUpperCase();
  };

  upperCase();

</script>

<template>
  <h1>Vue 3 入門</h1>
  <div v-text="message"></div>
  <div>
    <a v-bind:href="link">Google</a>
    <!-- 通常のスタイル設定 -->
    <p :style="{ color: activeColor, fontWeight: fontStress}">
      v-bindの設定方法の確認
    </p>
    <!-- 変数側でスタイル設定 -->
    <p :style="styleObjcet">v-bindの設定方法の確認</p>
</div>
</template>

<style scoped>
/* .active {
  color: red;
  font-weight: 900;
}
.underLine {
  text-decoration: underline;
}
.back {
  background-color: black;
} */
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
