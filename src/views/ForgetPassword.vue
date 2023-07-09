<template>
  <div class="bg_1">
  <div class="ForgetPassword">
    <p>尋找您的帳號</p>
    <p class="p2">請輸入您的手機號碼來尋找帳號</p>
    <div class="buttons">
    <input id="phoneNumber" type="tel" autocomplete="off" placeholder="手機號碼"><br>
    <router-link to="/HomeView"  custom v-slot="{ navigate }">
    <button @click="navigate" role="link">
    取消
  </button>
  </router-link>
  <router-link to="/HomeView"  custom v-slot="{ navigate }">
  <button @click="navigate" role="link" style="margin-left: 50px;background-color:rgb(5, 5, 34); color:white"> 
    搜尋
  </button>
  </router-link>
  </div>
  </div>
</div>
</template>
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
.ForgetPassword{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  min-height: 100%;
  padding-top:150px;
  padding-bottom:150px;
}
p{
  font-size: 30px;
  font-weight: 600;
  text-align: center;
}
.p2{
  font-size: 17px;
  font-weight: 600;
}
#phoneNumber{
  box-sizing: border-box;
  height: 30px;
  border: 2px solid black;
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 20px;
}
.buttons{
  display: inline-block;
  margin-top: 20px;
}
</style>