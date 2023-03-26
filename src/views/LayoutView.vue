<template>
    <header>
        <nav>
            <a href="" class="h1">简书</a>
            <RouterLink to="/">首页</RouterLink>
            <a href=""> 下载App</a>
            <a href="">会员</a>
            <RouterLink to="/todo">IT技术</RouterLink>
              <input type="search" class="sousuo" value placeholder="搜索" aria-label="搜索专题" >
              <img src="" alt="">
             
              <span class="kong">Aa</span>
              
            <RouterLink to="/login" class="login1">登录</RouterLink>
            <RouterLink to="/reg" class="t2" >注册</RouterLink>
            <a href="" class="wrote"><span>写文章</span></a>
        </nav>
    </header>
    <main>
        <RouterView />
    </main>
</template>

<script setup>

</script>

<style scoped>
*{
  margin: 0;
  padding:0;
  list-style: none;
  /* background-color: rgb(241, 241, 241); */
}
header {
  width: 100%;
  height: 60px;
  line-height: 60px;
  background-color: #FFFFFF;
  border-bottom: 1px solid gray;
  position: fixed;
  top: 0;
}

main {
  width: 85%;
  margin: 10px auto;
  border: 1px solid #ccc;
  min-height: 70vh;
  border-radius: 4px;
  margin-top: 70px;
  /* background-color: rgb(241, 241, 241); */
}

nav {
  width: 100%;
  font-size: 14px;
  text-align: center;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  font-size: 18px;
  text-decoration: none;
  color: #000;
  
}
a:hover{
  background-color: rgb(241, 241, 241);
}

nav a.router-link-exact-active {
  color: #1ea6e6;
}
.h1{
  color: #EA6F5A;
font-size: 32px;
font-weight: 700;
font-family:'Courier New', Courier, monospace;
}
.login{
  float: right;
}
.sousuo{
  width: 150px;
  height: 35px;
  background-color: rgb(241, 241, 241);
  border: none;
  margin-left: 20px;

  padding-left: 20px;
  border-radius: 20px;
}
.wrote{
  width:100px;
  height: 40px;
  line-height: 40px;
  margin-top: 10px;
  background-color: #EA6F5A;
  border-radius: 30px;
}
.wrote img{
  width:20px;
  height: 20px;
}
.kong{
  margin-left: 200px;
}

</style>