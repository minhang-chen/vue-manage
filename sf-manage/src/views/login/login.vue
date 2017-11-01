<template>
	<div class="g-wrapper">
		<div class="m-left">
			<img src="../../images/img_login_back.png" height="490" width="284">
		</div>
		<div class="m-right">
			<div class="logo">
				<img src="../../images/logo.png" height="41" width="93">
			</div>
			<div class="title">
				<span class="CN">登录</span>
				<span class="EN">Login</span>
			</div>
			<div class="m-email">
				<div class="icon-wrapper">
					<img src="../../images/ic_Envelope.png" height="20" width="20" >
				</div>
				<input class="email login-input" type="text" v-model="email" placeholder="请输入邮箱" @input="verification" ref="email">
			</div>
			<div class="m-password">
				<div class="icon-wrapper">
					<img src="../../images/ic_Lock.png" height="20" width="20">
				</div>
				<input class="password login-input" type="password" @input="verification" placeholder="请输入密码">
			</div>
			<div class="btn-wrapper">
				<a href="javascript:;" class="u-btn btn-login" @click="login" @keyup="show($event)">登录</a>
			</div>
		</div>
	</div>
</template>

<script>
	import axios from 'axios'
	import md5 from 'js-md5'
	// import $ from 'jquery'

	export default{
		data () {
			return {
				email: '',
				password: ''
			}
		},
		methods: {
			login() {
				const _this = this
				axios({
					method: 'post',
					url: 'http://192.168.1.197:8080/login',
					data: {
						email: this.email,
						password: this.password
					}
				}).then(function(res) {
					console.log(res)
					_this.$router.push({path: '/myPotient'})
				})
			},
			show: function(ev) {
                if (ev.keyCode === 13) {
                    this.login()
                }
            },
			verification() {
				const oEmail = document.querySelector('.email')
				const oPassword = document.querySelector('.password')
				var filter = /^([a-zA-Z0-9_.-])+@(([a-zA-Z0-9-])+.)+([a-zA-Z0-9]{2,4})+$/
				if (filter.test(this.$refs.email.value)) {
					oEmail.style.borderColor = '#e6e6e6'
				} else {
					oEmail.style.borderColor = '#ec4d31'
					this.email = oEmail.value
				}
				this.password = md5(oPassword.value)
				console.log(this.email, this.password)
			}
		}
	}
</script>

<style rel="stylesheet" style="stylesheet/scss" lang="scss">
	.g-wrapper{
		position:fixed;
		top: 50%;
		left:50%;
		width: 726px;
		height:490px;
		background:#fff;
		box-shadow: 0 2px 10px 0;
		border-radius: 6px;
		over-flow:hidden;
		transform: translateX(-50%) translateY(-50%);
		.m-left{
			display:inline-block;
		}
		.m-right{
			display:inline-block;
			vertical-align:top;
			width:340px;
			margin-left:50px;
			font-size:0;
			.logo{
				padding:41px 0;
				text-align:center;
			}
			.title{
				width:100%;
				padding-bottom:18px;
				color:#858585;
				border-bottom:2px solid #eaeaea;
				.CN{
					padding:12px 7px 0 0;
					font-size:20px;
					border-top:1px solid #ffb372;
				}
				.EN{
					font-size:14px;
				}
			}
			.m-email{
				margin-top:39px;
				.icon-wrapper{
					padding-top:10px;
				}
			}
			.m-password{
				margin-top:20px;
				.icon-wrapper{
					padding-top:10px;
				}
			}
			.btn-wrapper{
				margin-top:60px;
				text-align:center;
				.btn-login{
					padding:7px 65px;
					color:#fff;
					letter-spacing:10px;
				}
			}
		}
	}
</style>
