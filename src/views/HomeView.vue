<template>
  <div class="bg_1">
  <div class="login">
    <h1>{{ msg }}</h1>
      <div class="form-item">
        <p class="tip">請輸入您的手機號碼和密碼來進行登入<br>Please enter your mobile phone and password to log in</p>
          <input id="phoneNumber" type="tel" autocomplete="off" placeholder="手機號碼"><br>
          <input id="password" type="password" autocomplete="off" placeholder="密碼"><br>
          <button id="submit" type="submit" value="submit">登入</button><br>
  </div>
  <router-link to="/ForgetPassword">忘記密碼</router-link>
  <router-view/>
  <router-link to="/NewRegister"  custom v-slot="{ navigate }">
    <button @click="navigate" role="link">
    註冊新帳號
  </button>
  </router-link>
</div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bg_1{
  position: relative;
  background-size: cover;
  background-image: url(log_ba.png);
  background-position:center;
}
.bg_1::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(255, 255, 255, 0.5);
}
.login{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  min-height: 100%;
  padding-top:150px;
  padding-bottom:150px;
}
.form-item{
  margin-bottom: 5px;
  box-shadow: 10px 5px 5px black;
}
.tip{
  font: 30px sans-serif;
}
#phoneNumber{
  box-sizing: border-box;
  height: 30px;
  border: 2px solid black;
  border-radius: 5px;
}
#password{
  box-sizing: border-box;
  height: 30px;
  border: 2px solid black;
  border-radius: 5px;
}
#submit{
  margin-top: 10px;
  height: 30px;
  margin: 14px 12px;
  border: 2px solid black;
  font-weight:bold;
}
button{
  display: inline-block;
  margin-top: 20px;
  border: 2px solid black;
  font-weight:bold;
  height: 30px;
  border-radius: 5px;
}
</style>
