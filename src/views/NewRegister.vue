<template>
  <div class="form_register">
    <div class="form">
    <h1>建立新帳號</h1>
    <p>快速又簡單</p>
    <input id="phoneNumber" type="tel" autocomplete="off" placeholder="手機號碼">
    <input id="UserName" type="text" autocomplete="off" placeholder="名稱">
    <input id="Email" type="email" autocomplete="off" placeholder="電子郵件">
    <input id="Password" type="password" autocomplete="off" placeholder="密碼">
    <form action="/somewhere/to/upload" enctype="multipart/form-data">
      請上傳封面照片
      <input name="progressbarTW_img" type="file" accept="image/gif, image/jpeg, image/png"> 
    </form>
    <textarea name="mytext" rows="6" cols="50" required>請輸入自我介紹</textarea>
    <div class="buttons">
    <router-link to="/HomeView"  custom v-slot="{ navigate }">
      <button @click="navigate" role="link">
      取消
    </button>
    </router-link>
    <router-link to="/HomeView"  custom v-slot="{ navigate }">
    <button @click="navigate" role="link" style="margin-left: 50px;background-color:rgb(5, 5, 34); color:white"> 
      建立新帳號
    </button>
    </router-link>
      </div>
    </div>
  </div>
</template>
<style scoped>
.form_register{
  margin-bottom: 5px;
  box-shadow: 10px 5px 5px black;
  position: relative;
  background-size: cover;
  background-image: url(log_ba.png);
  background-position:center;
}
.form_register::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(255, 255, 255, 0.5);
}
.form{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  min-height: 100%;
  padding-top:10px;
  padding-bottom:150px;
}
input{
  box-sizing: border-box;
  height: 30px;
  border: 2px solid black;
  border-radius: 5px;
  margin-bottom: 10px;
}
.buttons{
  display: inline-block;
  margin-top: 20px;
}
</style>