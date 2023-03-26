<template>
    <div class="container">
        <div class="logo">
            <!-- <img src="../assets/images/book_bg.png"> -->
            <img src="../assets/images/logo.png" alt="">
        </div>
        <div class="main_content">
            <div class="login_left">
                <div>
                    <img src="../assets/images/book_bg.png" style="width: 346px;">
                </div>
                <div style="margin-top: 10px;">
                    <div class="download_btn">下载简书APP</div>
                    <div style="display: inline-block;position: relative;top: 15px;">
                        <img src="../assets/images/Code.png" style="width: 45px;">
                    </div>
                </div>
            </div>
            <div class="login_right" style="height: 572px;">
                <div class="login_right_header">
                    <span style="color:#969696;margin-right: 60px;">登录</span>
                    <span>注册</span>
                </div>
                <div class="form_content">
                    <div class="input_style">
                        <div class="phone_text" style="display: flex;">
                            <div>
                                <img src="../assets/images/phone_icon.png">
                            </div>
                            <div>
                                <input type="text" placeholder="你的昵称">
                            </div>
                        </div>
                        <div class="password_text" style="display: flex;">
                            <div style="margin-left: -2px;">
                                <img src="../assets/images/mobile_icon.png">
                            </div>
                            <div>
                                <input type="text" placeholder="手机号" style="padding-left: 10px;">
                            </div>
                        </div>
                        <div class="phone_text" style="display: flex;">
                            <div style="margin-left: 2px;">
                                <img src="../assets/images/pass_icon.png">
                            </div>
                            <div>
                                <input type="text" placeholder="设置密码">
                            </div>
                        </div>
                    </div>
                    <div class="login_btn">
                        注册
                    </div>
                    <p class="sign_up_msg">
                        点击 “注册” 即表示您同意并愿意遵守简书
                        <br>
                        <a href="#">用户协议</a> 和 <a href="#">隐私政策</a> 。 
                    </p>
                    <div class="social_account">
                        <span style="position: relative;">社交账号直接注册</span>
                    </div>
                    <div class="login_icon">
                        <div style="margin-right: 20px;">
                            <img src="../assets/images/weixin.png">
                        </div>
                        <div style="position: relative;top:-4px">
                            <img src="../assets/images/qq.png">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

a{
    text-decoration: none;
    outline: none;
    color: #3194d0;
}


.logo {
    margin-top: 55px;
    margin-left: 55px;
}

.main_content {
    display: flex;
    margin-top: 67px;
    margin-left: 30%;
}

.login_left,
.login_right {
    width: 401px;
    height: 501px;
    border: 1px solid lightgray;
    background-color: #fff;
    box-shadow: 0 0 8px rgba(0, 0, 0, .1);
}

.login_left {
    border: none;
    margin-right: 20px;
    box-shadow: none;
    background-color: hsla(0, 0%, 71%, 0);
}

.download_btn {
    display: inline-block;
    width: 257px;
    height: 48px;
    line-height: 48px;
    color: #fff;
    font-size: 16px;
    text-align: center;
    background-color: #ea6f5a;
    border-radius: 30px;
    margin-right: 20px;
}

.login_right_header {
    text-align: center;
    margin-top: 57px;

    font-size: 18px;
}

.login_right_header span {
    position: relative;
    display: inline-block;
}

.login_right_header span:nth-child(2) {
    color: #ea6f5a;
    font-weight: 700;
}


.login_right_header span:nth-child(2)::after {
    position: absolute;
    content: "";
    width: 53px;
    height: 24px;
    border-top: 2px solid #ea6f5a;
    top: 35px;
    left: -8px;
}

.form_content {
    margin-top: 70px;
    padding-left: 55px;
}

.input_style {
    margin-bottom: 15px;
}

.input_style>div {
    width: 300px;
    height: 50px;
    background-color: hsla(0, 0%, 71%, .1);
    border-radius: 0 0 4px 4px;
}

.phone_text,
.password_text {
    padding-top: 16px;
    padding-left: 16px;
}

.input_style input {
    width: 100%;
    height: 50%;
    outline: none;
    border: none;
    /* border: 1px solid black; */
    background-color: hsla(0, 0%, 71%, 0);
    padding: 4px 12px 4px 15px;
    font-size: 14px;
}

.login_container {
    display: flex;
    width: 300px;
    justify-content: space-between;
}

.login_btn {
    width: 300px;
    height: 45px;
    text-align: center;
    line-height: 45px;
    background: #42c02e;
    border-radius: 30px;
    font-size: 20px;
    color: #fff;
    margin-top: 20px;
    margin-bottom: 50px;
    cursor: pointer;
}

.social_account {
    width: 300px;
    font-size: 14px;
    text-align: center;
    color: #969696;
}

.social_account span::before {
    position: absolute;
    content: "";
    width: 65px;
    height: 10px;
    border-bottom: 1px solid #969696;
    left: -85px;
}

.social_account span::after {
    position: absolute;
    content: "";
    width: 65px;
    height: 10px;
    border-bottom: 1px solid #969696;
    right: -85px;
}

.login_icon {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    width: 300px;
}

.login_icon img {
    width: 41px;
}

.sign_up_msg{
    margin-top: -30px;
    margin-bottom: 30px;
    width: 300px;
    font-size: 12px;
    line-height: 20px;
    color: #969696;
    text-align: center;
}
</style>