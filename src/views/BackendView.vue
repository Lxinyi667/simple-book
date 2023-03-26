<template>
    <div>
        <div  class="itemlist-box">
            <!----> 
            <div  class="content">
                <a  target="_blank" class="title">
                    这几种常见的 JVM 调优场景，你知道吗？
                </a> 
                <div  class="abstract">
                    假定你已经了解了运行时的数据区域和常用的垃圾回收算法，也了解了Hotspot支持的垃圾回收器。 一、cpu占用过高 cpu占用过高要分情况讨论，是不是业务上在搞活动，突然有大批的流量进来，而且活动结...
                </div> 
                <img  referrerpolicy="no-referrer" src="../assets/images/love4.png" alt="">
            </div>
            <div  class="content">
                <a  target="_blank" class="title">
                    Spring Cloud alibaba之Feign
                </a> 
                <div  class="abstract">
                    JAVA项目中如何实现接口调用？ HttpclientHttpclient是Apache Jakarta Common下的子项目，用来提供高效的、最新的、功能丰富的支持Http协议的客户端编程工具包...
                </div> 
                <img  referrerpolicy="no-referrer" src="../assets/images/love3.png" alt="">
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style  scoped>
*{
    margin:0;
    padding:0;
    list-style: none;
    text-decoration: none;
    color: black;
}
.itemlist-box {
    position: relative;
    margin: 0 0 15px;
    padding: 30px 15px 20px 15px;
}
.title{
    font-weight: 1000;                                                                          
    font-size: 20px;
    
}
.abstract{
    margin-top: 10px;
    color: gray;
    font-size: 14px;
}
img{
  height: 30px;
}
</style>