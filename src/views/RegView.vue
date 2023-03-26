<template>
  <div class="login">
      <h1>简书</h1>
      <div class="body">
        <div class="left">
          <img src="src\assets\images\iphone.png" alt="" class="imgiphone">
          <div class="iphonedown">
            <a class="downl" href="https://www.jianshu.com/apps?%20utm_medium=desktop&utm_source=sign_in_page_click">下载简书APP</a>
          </div>
        </div>
        <div class="main">
          <h4 class="title">
            <!-- <a href="" class="active">登录</a> -->
            <RouterLink to="/login" class="active"  style="background-color: #fff;text-decoration: none;"
            >登录</RouterLink>
           <b>·</b>
            <RouterLink to="/reg" class="t2"  style="background-color: #fff;text-decoration: none;"
            >注册</RouterLink>
            <!-- <b>·</b> -->
            <!-- <RouterLink to="/" class="t1" style="background-color: #fff;color:black;text-decoration: none;">去主页</RouterLink> -->
          </h4>
          <div class="sign-in-container">
            <input name="utf8" type="hidden" value="✓">
            <input type="hidden" name="authenticity_token" 
            value="ruhn0hXXLCMi2KJ9AqcWsSqAFoqVxLcz8fGxPpgx+Nvi+hRd2CBNOTWl3E3nDWftUs6ZVFNONCwNnHOeThAq0A==">
            <div class="input">
              <input type="text" placeholder="你的昵称" name="name" id="session_email_or_mobile_number">
              <input type="text" placeholder="手机号" name="name" id="session_mobile_number">
              <input type="password" placeholder="密码" name="password" id="session[password]">
            </div>
            
            <button class="sign-in-btn">注册</button>
            <div class="notice1">
              <p class="notice">点击 “注册” 即表示您同意并愿意遵守简书
              <span>用户协议</span> 和 <span>隐私政策</span> 。</p>
            </div>
          </div>
        </div>
      </div>
      
  </div>
</template>

<script setup>

</script>

<style scoped>
*{
margin: 0;
padding: 0;
background-color: rgb(241, 241, 241);
list-style: none;
text-decoration: none;
}
.login {
height: 100vh;
background-size: 100% 100%;
padding: 20px;
}
.login h1{
color: #EA6F5A;
font-size: 40px;
font-weight: 700;
font-family:'Courier New', Courier, monospace;
}
.body{
width: 60%;
margin: 0 auto;
display: flex;
float: left;
margin-top: 140px;
}
.left{
width:400px;
height: 500px;

margin-left: 300px;
}
.imgiphone{
width: 400px;
height: 450px;
flex:right;

}
.iphonedown .downl{
width: 300px;
height: 42px;
line-height: 42px;
margin-left: 50px;
background-color:  #EA6F5A;;
color: white;
border: none;
font-size: 18px;
font-weight: 500;
border-radius: 30px;
position: absolute;
text-align: center;
}
.main{
position: relative;
left: 50%;
margin: 0 0 0 -300px;
box-shadow: none;
text-align: center;
width:400px;
height: 500px;
background-color: #fff;
vertical-align: middle;
display: inline-block;
}
.main *{
background-color: #fff;
}
.title{
font-weight: 18px;
color: black;
position: absolute;
background-color: #fff;
left: 25%;
top: 50px;
margin: 0 auto 50px;
  padding: 10px;
}
.active{
padding-right: 16px;
color: black;
background-color: #fff;
text-decoration: none;
padding:0 10px 5px 10px;


}
.t2{
  padding-right: 16px;
  color: #EA6F5A;
  background-color: #fff;
  text-decoration: none;
  padding:0 10px 5px 10px;
  border-bottom: 2px solid #EA6F5A;
  font-size: 18px;
}
b{
padding-right: 16px;
background-color: #fff;
}
.input{
width: 400px;
height: 100px;
margin: 0 auto;

margin-top: 150px;
/* background-color: #fff; */
border-radius: 8px;
}
.input input{
width: 270px;
height: 50px;

padding-left:30px ;
border: 1.5px solid gray;
outline: none;
}
.remember-btn{
width: 300px;
height: 50px;
background-color: #fff;
display: flex;
margin: 0 auto;
padding-top: 10px;
}
.remember-btn span{
/* position: absolute; */
padding: 10px 0 0 10px;
}
.forget{
position: absolute;
right: 50px;
font-size: 14px;
padding-top: 10px;
float: right;
}
.sign-in-btn{
width: 300px;
height: 40px;
background-color:#42BF2E ;
color: #fff;
font-size: 18px;
border: none;
margin-top: 80px;
border-radius: 20px;
}
.notice1{
width: 250px;
margin:0 auto;
font-size: 10px;
color: gray;
padding-top: 10px;
}
.notice1 span{
color: rgb(78, 111, 219);
}
</style>