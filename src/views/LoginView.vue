<template>
    <div class="login-view">

        <div class="main">
            <div>
                <div class="">
                    <div class="new-header-container">
                        <div class="header">
                            <div class="header-main"><a href="//www.zuche.com" title="神州租车" class="header-logo"></a>
                                <div class="header-contact">
                                    <div class="tel-dropdown">400-616-6666</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="login-wrapper">
                <div class="login-main">
                    <div class="login-form">
                        <ul class="login-form-tabs">
                            <li class="on">登 录</li>
                        </ul>
                        <div class="login-form-panel">
                            <form class="ant-form ant-form-horizontal zuche-form">
                                <div class="ant-form-item">
                                    <div class="ant-row ant-form-item-row">
                                        <div class="ant-col ant-form-item-control">
                                            <div class="ant-form-item-control-input">
                                                <div class="ant-form-item-control-input-content"><span
                                                        class="ant-input-affix-wrapper"><span class="ant-input-prefix"><i
                                                                class="zc-icon zc-icon-iuser"></i></span>
                                                        <input name="username" maxlength="18" placeholder="请输入用户名"
                                                            class="ant-input" type="text" value=""
                                                            v-model="username"></span>
                                                    <div class="msg-tip on-top" v-if="showUsernameError"><i
                                                            class="zc-icon zc-icon-retan"></i>请输入正确的用户名</div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="ant-form-item">
                                    <div class="ant-row ant-form-item-row">
                                        <div class="ant-col ant-form-item-control">
                                            <div class="ant-form-item-control-input">
                                                <div class="ant-form-item-control-input-content">
                                                    <div class="ant-row" style="margin-left: -4px; margin-right: -4px;">
                                                        <div class="ant-col ant-col-15"
                                                            style="padding-left: 4px; padding-right: 4px;"><span
                                                                class="ant-input-affix-wrapper"><span
                                                                    class="ant-input-prefix"><i
                                                                        class="zc-icon zc-icon-idtm"></i></span><input
                                                                    name="mobileCode" maxlength="6" placeholder="请输入密码"
                                                                    class="ant-input" type="text" value=""
                                                                    v-model="password"></span></div>
                                                        <div class="ant-col ant-col-9"
                                                            style="padding-left: 4px; padding-right: 4px;">
                                                            <div class="captcha-btn undefined" @click="showPassWord">获取密码
                                                            </div>
                                                        </div>
                                                    </div>
                                                    <div class="msg-tip on-top" v-if="showEmptyFieldsError"><i
                                                            class="zc-icon zc-icon-retan"></i>请输入正确的密码</div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </form>
                            <ul class="login-form-handle">
                                <li class="auto-login">
                                    <div class="clear"></div>
                                </li>
                                <li>
                                    <div class="zuche-btn undefined primary" @click="login">登录</div>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="login-banner-brand">
                    <ul class="login-banner-brand-inner">
                        <li><i class="zc-icon zc-icon-yecx"></i>
                            <p><b>100+</b>车型</p>
                        </li>
                        <li><i class="zc-icon zc-icon-yewd"></i>
                            <p>千家网点</p>
                        </li>
                        <li><i class="zc-icon zc-icon-yecxn"></i>
                            <p><b>100%</b>保障</p>
                        </li>
                        <li><i class="zc-icon zc-icon-yelc"></i>
                            <p>无限里程</p>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer">
                <div class="container"><a class="car-back-top"
                        href="http://multimedia.gateway.zuche.com:2003/IM/Web/index.html " target="_blank"></a>
                    <div class="inner-links">
                        <div class="left">
                            <div class="column"><span class="title">神州租车</span><a title="关于我们"
                                    href="//huodong.zuche.com/aboutus/company.do" class="link">关于我们</a><a title="联系我们"
                                    target="_parent" href="//huodong.zuche.com/aboutus/contact.do" class="link">联系我们</a><a
                                    target="_blank" title="加入我们" href="https://zhaopin.zuche.com/" class="link">加入我们</a><a
                                    target="_parent" title="新闻中心" href="//news.zuche.com" class="link">新闻中心</a><a
                                    target="_blank" title="资质信息" href="//huodong.zuche.com/aboutus/license.do"
                                    class="link">资质信息</a></div>
                            <div class="column"><span class="title">合作伙伴</span><a title="投资者关系" target="_blank"
                                    href="//ir.zuche.com" class="link">投资者关系</a></div>
                            <div class="column"><span class="title">其他服务</span><a title="网站导航" target="_parent"
                                    href="//help.zuche.com/sitemap.do" class="link">网站导航</a><a title="隐私保护" target="_parent"
                                    href="//huodong.zuche.com/privacypolicy.do" class="link">隐私保护</a></div>
                        </div>
                        <div class="right">
                            <div class="qr">
                                <div class="item"><img
                                        src="//cars.zuchecdn.com/static/img/app_4d9ed9cbe04ebd2d0a11dd708a404569.png"
                                        alt="app"><span class="qrtxt">下载神州租车App</span></div>
                                <div class="item"><img
                                        src="//cars.zuchecdn.com/static/img/wechat_e2e228bf5f7d57522eb8617b562748fc.png"
                                        alt="wechat"><span class="qrtxt">微信小程序</span></div>
                                <div class="item"><img
                                        src="//cars.zuchecdn.com/static/img/gongzhonghao_f62c31a200abcb6817b4cac60a8ef3ce.png"
                                        alt="gongzhonghao"><span class="qrtxt">关注微信公众号</span></div>
                                <div class="item"><img
                                        src="//cars.zuchecdn.com/static/img/alipay_b643b4338bc0a20340b2b8997dd2f0ef.png"
                                        alt="alipay"><span class="qrtxt">支付宝小程序</span></div>
                            </div>
                            <div class="advice">如果您对神州租车网站有任何意见，欢迎发送邮件到<a href="Mailto:web@zuche.com">web@zuche.com</a>
                            </div>
                        </div>
                    </div>
                    <div class="gap-line"></div>
                    <div class="copy-right">
                        <p class="info">Copyright©2008-2021 www.zuche.com All Rights Reserved.　北京神州汽车租赁有限公司 <a
                                href="//beian.miit.gov.cn">京ICP备10005002号</a><i class="guo-icon"></i><a
                                href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010502046201">京公网安备
                                11010502046201
                                号</a></p>
                        <div class="footer-certificate" id="footer-certificate"><a target="_blank"
                                href="https://credit.cecdc.com/CX20121016001772002081.html" title="诚信网站"
                                style="vertical-align: 13px;"><img src="//icon.szfw.org/sf.png"
                                    style="height: 32px; border-width: 0px;"></a></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LoginView',
    data() {
        return {
            username: '', password: '', showUsernameError: false,
            showEmptyFieldsError: false
        }
    },
    methods: {
        login() {
            // 假设账号为 'admin'，密码为 '123'
            if (this.username == 'admin' && this.password == '123') {
                alert('登录成功!');
                // 将登录状态保存在 localStorage 中
                localStorage.setItem('isAuthenticated', 'true');
                // 登录成功后跳转到首页或其他页面
                this.$router.push('/');
            } else if (this.username === '' && this.password === '') {
                this.showEmptyFieldsError = true;
                this.showUsernameError = true;
                setTimeout(() => {
                    this.showEmptyFieldsError = false;
                    this.showUsernameError = false;
                }, 1000);
            } else if (this.username !== 'admin') {
                this.showUsernameError = true;
                setTimeout(() => {
                    this.showUsernameError = false;
                }, 1000);
            } else {
                this.showEmptyFieldsError = true;
                setTimeout(() => {
                    this.showEmptyFieldsError = false;
                }, 1000);
            }
        },
        showPassWord() {
            alert('密码123');
        }

    },
    mounted() {

    }
};
</script>

<style scoped>
.login-view {}
</style>