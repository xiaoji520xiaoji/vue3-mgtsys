<template>
    <div class="login-bg">
        <div class="content">
            <div class="title">
                <!-- <h2 class="system_title"></h2> -->
                <br />
                <img src="../assets/loginJPG.png" style="width: 100%; height: 80%" />
            </div>
            <div class="loginFram">
                <el-form>
                    <h1 style="margin: 5px 0 0 0; color: #333; margin-bottom: 50px;">用户登录</h1>
                    <el-form-item label="用户名" prop="username">
                        <el-input placeholder="请输入用户名"/>
                    </el-form-item>
                    <el-form-item label="密码" prop="password">
                        <el-input show-password placeholder="请输入密码"></el-input>
                    </el-form-item>
                    <el-form-item>
                        <el-button class="login-submit"></el-button>
                    </el-form-item>
                </el-form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Login',
    setup() {
        return {

        }
    }
}
</script>


<style>
.login-bg {
    background-image: url('../assets/login-bg.png');
    background-size: 100% 100%;
}

.system_title {
    text-align: center;
    color: white;
}

.content {
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 950px;
    height: 500px;
    border-radius: 8px;
    padding: 12px 30px 0 0;
    background-size: 100% 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: white;
    border-radius: 100px 20px 20px 100px;
}

.title {
    height: 100%;
    width: 60%;
    padding: 3%;
    border-radius: 50px 0 0px 50px;
    background-color: #0000ff;
}

.loginFram {
    width: 40%;
    height: 100%;
    padding: 30px 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0 auto;
}

.label {
    font-size: 20px;
    margin: 16px 0px;
    text-align: left;
}

.login-submit {
    width: 100%;
    background-color: #0000ff;
}
</style>