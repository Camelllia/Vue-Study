<!--
  ================================================
  1. 아이디 / 비밀번호 input 영역 컴포넌트화 (prop)
  2. Form Validation(유효성) 체크 
  3. (선택) 로그인 버튼 눌렀을 때의 처리 (HTTP POST 요청)
  ================================================
-->
<template>
  <section class="intro">
      <div class="login-area">
          <div class="login">
              <form v-on:submit="Login()">
                  <!--[s] ==============아이디 컴포넌트==============-->
                  <InputID v-model="loginInfo.userId"></InputID>
                  <!--[e] ==============아이디 컴포넌트==============-->

                  <!--[s] ==============비밀번호 컴포넌트==============-->
                  <InputPassword v-model="loginInfo.userPw"></InputPassword>
                  <!--[e] ==============비밀번호 컴포넌트==============-->
            
                  <button type="submit" class="btn btn-login">login</button>
              </form>
          </div>
      </div>
  </section>
</template>

<script>
import InputID from './components/IdInput.vue';
import InputPassword from './components/PwInput.vue';

export default {
  name: 'App',

  data() {
    return {
      loginInfo: {
        userId : "",
        userPw : ""
      }
    };
  },

  components: {
    InputID,
    InputPassword
  },

  methods: {
    Login: function() {
      if(!this.loginInfo.userId || !this.loginInfo.userPw) {
        alert("입력되지 않은 필드가 존재합니다.");
        return;
      }
    },
  },

  computed: {
    
  },
  beforeCreate: function () {},
  created: function () {},
  mounted: function () {},
  updated: function () {},
  beforeDestroy() {},
  destroyed() {}
};
</script>

<style>
/* 로그인 */
.intro {
  position: relative;
  width: 996px;
  margin: 0 auto;
}
.intro .login-area {
  width: 340px;
  margin: 100px auto 0;
}
.intro .login-area .login {
  width: 340px;
  margin-bottom: 10px;
  padding: 20px;
  border: 1px solid #e3e3e3;
  box-sizing: border-box;
}
.intro .login-area .login .input-a {
  width: 298px;
  height: 36px;
  margin-bottom: 10px;
  border: 1px solid #e3e3e3;
}
.intro .login-area .login label {
  margin-bottom: 12px;
  font-size: 12px;
  font-weight: bold;
}
.intro .login-area .login .btn-login {
  width: 100%;
  height: 45px;
  padding: 0 15px;
  border: 1px solid #004b8d;
  background-color: #004b8d;
  font-size: 15px;
  color: #fff;
  line-height: 43px;
}

/* form - input */
.input-a {
  padding: 0 10px;
  height: 30px;
  line-height: 26px;
  border: 1px solid #ccc;
  color: #333;
  font-size: 14px;
  box-sizing: border-box;
}
.input-a.h22 {
  height: 22px;
  line-height: 20px;
  font-size: 12px;
}
.input-a.h24 {
  height: 24px;
  line-height: 22px;
  font-size: 12px;
}
.input-a.readonly {
  background: #f3f8fb;
  color: #999;
}
</style>