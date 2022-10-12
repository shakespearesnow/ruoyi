<template>
  <div class="logingBox">
    <h1>登陆</h1>
    <div class="inputBox">
      <div class="inputText">
        <span class="iconfont icon-yonghuming"></span>
        <input type="text" placeholder="用户名" />
      </div>
      <div class="inputText">
        <span class="iconfont icon-mima"></span>
        <input type="password" placeholder="密码" />
      </div>
      <div class="input-btn">登陆</div>
      <div class="sign-up">还没账户?<a href="">立即注册</a></div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.logingBox {
  width: 100%;
  min-height: 100vh;
  background-image: url(../../public/images/bacclogin.png);
  background-size: 100%;
  background-repeat: no-repeat;
  /* background-position: top center;
  background-attachment: fixed; */
}
</style>
