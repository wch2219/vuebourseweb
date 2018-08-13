<template>
    <div>

        <div class="content">
            <div class="login">
                <div class="login-left">
                    <div>
                        <h4 >最新公告</h4>

                    </div>
                    <ul>
                        <li v-for="(item,index) in msg" :key="item.id">
                            <span>{{item.title}}</span>

                            <span>{{item.strs}}</span>

                        </li>

                    </ul>
                </div>
                <div class="login-right">
                    <div class="right-title">
                        <img src="../images/Signin.png" alt="">
                        <span>登录</span>
                    </div>

                    <div class="login-input">
                        <table>
                            <span>手机号/邮箱</span><br>
                            <input type="text" placeholder="请输入用户名">
                        </table>
                        <table>
                            <span>密码</span> <br>
                            <input type="password" placeholder="请输入密码">
                        </table>
                        <input id="login-button" type="button" value="登录">
                        <div class="login-r-b">
                            <p class="forgit-pwd">忘记密码？</p>

                            <router-link to="/register">
                            <p class="start-register">立即注册</p>
                            </router-link>

                        </div>
                    </div>


                </div>
            </div>
        </div>

        <router-view></router-view>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                nama:'sadasdasdas',
                msg:[
                    {id:1,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:2,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:3,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:4,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:5,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:6,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:7,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:8,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:9,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'},
                    {id:10,title:'关于更改DOTBIT国际交易所',strs:'2018-08-07'}
                ]
            };
        },
        methods:{


        }
    }
</script>

<style scoped>
    .content {
        height: 786px;
        width: 100%;
        background-color: #F8F8F8;
        text-align: center;
        vertical-align: middle;
        padding-top: 1px;
    }

    .login {
        width: 1190px;
        height: 430px;
        margin: 135px auto;
    }
    /*左侧*/
    .login-left {
        width: 720px;
        height: 430px;
        float: left;
        box-shadow: 2px 2px 6px rgba(178,178,178,0.11);
        background-color: white;
        border-radius: 3px;
        padding-top: 38px;
        padding-left: 36px;
        padding-right: 36px;
        box-sizing:border-box;
        color: #424242;
    }
    .login-left h4{
        float: left;
        font-weight: normal;

    }
    .login-left li{
        float: left;
        width: 650px;
        border-bottom: 1px solid #E7E7E7;
        cursor: pointer;
    }
    .login-left ul{
        margin-top: 38px;
        width: 100%;
        font-size: 14px;

    }
    .login-left li span:nth-child(1){
        float: left;
        line-height: 34px;
    }
     .login-left li span:nth-child(2){
        float: right;
         line-height: 34px;
    }

    /*右侧*/
    .login-right {
        width: 440px;
        height: 430px;
        float: right;
        margin-left: 20px;
        box-shadow: 2px 2px 5px rgba(178,178,178,0.11);
        background-color: white;
        border-radius: 3px;
        border-top: 3px solid #00A7FF;
        color: #424242;
    }

    .right-title {
        height: 26px;
        width: 100px;
        text-align: center;
        margin: 0px auto;
        line-height: 26px;
        vertical-align: center;
        margin-top: 34px;
    }

    .right-title img {
        float: left;
    }

    .right-title span {
        line-height: 26px;
        height: 26px;
        margin-left: 6px;
        float: left;
        font-size: 22px;
    }

    /*福输入框*/
    .login-input {
        width: 360px;
        margin-top: 6px;
        margin-left: 40px;
        font-size: 14px;

    }

    .login-input input {
        border-bottom: 1px solid #dbdbdb;
        width: 360px;
        margin-top: 10px;
    }

    .login-input span {
        float: left;
        margin-top: 50px;
    }

    .login-input input:focus {
        border-bottom: 1.5px solid #dbdbdb;
    }

    /*登录按钮*/
    #login-button {
        width: 360px;
        height: 42px;
        color: white;
        margin-top: 50px;
        border-radius: 21px;
        background-image: linear-gradient(90deg,
        rgba(0, 114, 255, 0.61) ,
        rgba(0, 198, 255, 0.61));

    }
    #login-button:active{

        box-shadow: 2px 2px 5px rgba(178,178,178,0.5);
    }
    .login-r-b{
        width: 360px;
        margin-top: 22px;

    }
    .forgit-pwd{
        margin-top: 0px;
        float: left;
        cursor: pointer;
    }
    .start-register{
        float: right;
        cursor: pointer;
    }
</style>