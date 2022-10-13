<template>
  <div class="logingBox">
    <h1>登陆</h1>
    <div class="inputBox">
      <div class="inputText">
        <span class="iconfont icon-yonghuming"></span>
        <input type="text" v-model="userName" placeholder="用户名" />
      </div>
      <div class="inputText">
        <span class="iconfont icon-mima"></span>
        <input type="password" v-model="password" placeholder="密码" />
      </div>
      <button class="input-btn" @click="submit()">登陆</button>
      <div class="sign-up">还没账户?<a href="">立即注册</a></div>
    </div>
  </div>
</template>


<script>

import axios from 'axios'
import qs from 'qs'

  export default {
    name: 'login',
    data: function(){
      return {
        userName: "admin",
        password: 'admin',
        code: '123'
      }
    },
    methods: {
      submit: function(){
        let params = {
          userName: this.userName,
          password: this.password
        }

        var url = "http://1.14.110.33:25590/RestForJT/login"

        // axios.get(url,{params:params
        // }).then(function(response){
        //   console.log(response);
        // }).catch(function(error){
        //   console.log(error);
        // })

        axios.post(url,qs.stringify(params)
        ).then(function(response) {
          console.log(response);
        }).catch(function(error) {
          console.log(error);
        });

      }
    }
  }  


</script>


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
