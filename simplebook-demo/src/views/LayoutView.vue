
<template>
    <div>
        <nav>
            <div class="nav_container">
                <div style="position: relative;top:5px;margin-right: 150px;">
                    <img src="../assets/images/logo.png" style="width: 70px;">
                </div>
                <router-link to="home" class="nav_item">
                    <div style="position: relative;top:-5px">
                        <span class="iconfont icon-compass"
                            style="font-size: 17px;margin-right: 5px;"></span>
                        <span style="font-size: 17px;">首页</span>
                    </div>
                </router-link>
                <router-link to="download" class="nav_item">
                    <div style="position: relative;top:-5px">
                        <span class="iconfont icon-yunxiazai"
                            style="font-size: 23px;font-weight: 500;margin-right: 5px;"></span>
                        <span style="font-size: 17px;font-weight: 400;">下载APP</span>
                    </div>
                </router-link>
                <router-link to="vip" class="nav_item">
                    <div style="position: relative;top:-5px">
                        <span class="iconfont icon-wangguan1"
                            style="font-size: 17px;font-weight: 600;margin-right: 5px;"></span>
                        <span style="font-size: 17px;font-weight: 400;">会员</span>
                    </div>
                </router-link>
                <router-link to="it" class="nav_item">
                    <div style="position: relative;top:-5px">
                        <span class="iconfont icon-jishufuwu"
                            style="font-size: 17px;font-weight: 600;margin-right: 5px;"></span>
                        <span style="font-size: 17px;font-weight: 400;">IT技术</span>
                    </div>
                </router-link>
                <div style="padding-left: 10px;" class="search-box">
                    <span style="float: left;">搜索</span>
                    <span style="float:right;margin-right: 20px;font-size: 20px;" class="iconfont icon-sousuo"></span>
                </div>
                <!-- <div style="position: relative;top:-5px"> -->
                <div>
                    <img src="../assets/images/download_app.png" style="height: 40px;position: relative;top: 10px;">
                    <span style="font-size: 12px;color: #ffd875;position: relative;left: -40px;top: -5px;">抽奖</span>
                </div>
                <div style="position: relative;top:-5px;margin-right: 25px;">
                    <span style="margin-right: 20px;color: #969696;line-height: 20px;">Aa</span>
                    <router-link to="login">
                        <span style="color: #969696;line-height: 20px;">登录</span>
                    </router-link>
                </div>
                <router-link to="reg" style="margin-right: 20px;">
                <div class="registerBtn">
                    注册
                </div>
                </router-link>
                <div class="articleBtn">
                    <span class="iconfont icon-yongyan"></span>
                    写文章
                </div>
                <!-- </div> -->
                <!--  -->
            </div>
            <!-- <router-link to="home">asas</router-link> -->
        </nav>
    </div>

    <main>
        <router-view></router-view>
    </main>
</template>

<script setup>

</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
}

nav {
    width: 100%;
    height: 70px;
    border-top: 1px solid rgba(128, 128, 128, .2);
    border-bottom: 1px solid rgba(128, 128, 128, .2);
}

.nav_container {
    width: 80%;
    height: 100%;
    line-height: 70px;
    /* background-color: aquamarine; */
    margin: 0 auto;
}

.nav_container div {
    display: inline-block;

}

.nav_item {
    margin-right: 60px;
}

.search-box {
    position: relative;
    top: 8px;
    width: 230px;
    height: 36px;
    border: 1px solid lightgray;
    border-radius: 40px;
    line-height: 36px;
    font-size: 14px;
    background: #eee;
    margin-right: 20px;
}
.registerBtn,
.articleBtn{
    position: relative;
    top: -5px;
    cursor: pointer;
    width: 80px;
    height: 40px;
    text-align: center;
    line-height: 40px;
    border: 1px solid rgba(236,97,73,.7);
    border-radius: 20px;
    color: #ea6f5a;
}

.articleBtn{
    width: 100px;
    color: #fff;
    background-color: #ea6f5a;
}

a{
    color: #000;
}

/* 选中链接的样式 */
.router-link-exact-active{
    color: #ea6f5a !important;
}

/* 选中之后链接的样式 */
a:visited{
    color: #000;
}


</style>