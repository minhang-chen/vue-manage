<template>
	<div>
		<header-public></header-public>
		<div class="m-wrapper">
			<div class="title">
				<div>我的患者</div>
				<div class="list">
					<a href="javascript:;" class="back">返回</a>
					<a href="javascript:;" class="list-item">我的患者</a>><a href="javascript:;" class="list-item">个人信息</a>
				</div>
			</div>
			<div class="m-table">
				<ul>
					<!-- <li>
						<div class="u-title">姓名</div>
						<input class="u-input" type="text" name="" placeholder="请输入全名">		
					</li>
					<li>
						<div class="u-title">年龄</div>
						<input class="u-input" type="text" name="" placeholder="请输入年龄">		
					</li>
					<li>
						<div class="u-title">ID号</div>
						<input class="u-input" type="text" name="" placeholder="请输入ID号">
						<img class="icon-choose" src="../../images/ic_choose.png" height="10" width="14">
					</li>
					<li>
						<div class="u-title">体验号</div>
						<input class="u-input" type="text" name="" placeholder="请输入体验号">		
					</li>
					<li>
						<div class="u-title">手机号</div>
						<input class="u-input selected" type="text" name="" placeholder="请输入手机号">
						<img class="ic-Wipeoff" src="../../images/ic_Wipeoff.png" height="18" width="18">	
					</li>
					<li>
						<div class="u-title">微信号</div>
						<input class="u-input" type="text" name="" placeholder="请输入微信号">		
					</li>
					<li>
						<div class="u-title">电子邮箱</div>
						<input class="u-input" type="text" name="" placeholder="请输入邮箱">		
					</li> -->
					<li v-for="(title, index) in titles">
						<div class="u-title">{{title}}</div>
						<!-- <input  :class="[inputTitles[index].current==true?selected:'', uInput]"   type="text"  :placeholder="inputTitles[index].title" @click="addClass(index)" > -->
						<input-model :class="[inputTitles[index].current==true?selected:'']" :inputTitles='inputTitles' :inputIndex='index' :placeholders='inputTitles[index].title'  @click.native="addClass(index)"></input-model>
						<img class="ic-Wipeoff" src="../../images/ic_Wipeoff.png" height="18" width="18" v-show="inputTitles[index].current" @click="clearContent(index)">
					</li>
				</ul>
				<div class="m-bottom">
					<a href="javascript:;" class="btn-white save">保存</a>
					<a href="javascript:;" class="u-btn filling" @click="showDetail">继续填写随访表</a>
				</div>
			</div>
		</div>
		<transition name="fade">
			<div v-show="detailShow" class="dialog-wrapper">
				<div class="m-dialog">
					<div class="header">
						<span>请选择随访模板</span>
						<img class="close" src="../../images/ic_close.png" height="20" width="20" @click="hideDetail">
					</div>
					<div class="m-select">
						<select>
							<option>体重管理</option>
							<option>个人信息管理</option>
						</select>
						<span class="u-triangle"></span>
					</div>
					<div class="m-content">
						<div class="list-item" v-for="(sfRecording, index) in sfRecordings" @click="choose(index)">
							<span>{{sfRecording.title}}</span>
							<img v-show="sfRecordings[index].current" class="item-selected" src="../../images/ic_choose.png" height="10" width="14">
						</div>
					</div>
					<div class="m-bottom">
						<a href="javascript:;" class="u-btn btn-ok">确定</a>
					</div>
				</div>
			</div>	
		</transition>
		
	</div>
</template>

<script>
	import header from '../../components/header/header.vue'
	import input from '../../components/input/inputs.vue'

	export default{
		data () {
			return {
				titles: ['姓名', '年龄', 'ID号', '体验号', '手机号', '微信号', '电子邮箱'],
				inputTitles: [{title: '请输入全名', current: false}, {title: '请输入年龄', current: false}, {title: '请输入ID号', current: false}, {title: '请输入体验号', current: false}, {title: '请输入手机号', current: false}, {title: '请输入微信号', current: false}, {title: '请输入邮箱', current: false}],
				selected: 'selected',
				uInput: 'u-input',
				detailShow: false,
				chooseShow: false,
				sfRecordings: [{title: '体重管理-第一周电话随访记录', current: false}, {title: '体重管理-第一周电话随访记录', current: false}, {title: '体重管理-第一周电话随访记录', current: false}]
			}
		},
		components: {
			'header-public': header,
			'input-model': input
		},
		methods: {
	        addClass: function (index) {
	        for (let i = 0, len = this.inputTitles.length; i < len; i++) {
	            this.inputTitles[i].current = false
	        }
	        this.inputTitles[index].current = true
	        },
	        clearContent: function (index) {
	        const oInput = document.querySelectorAll('.u-input')
	        oInput[index].value = ''
	        },
	        showDetail() {
				this.detailShow = true
			},
			hideDetail() {
				this.detailShow = false
			},
			choose(index) {
				if (this.sfRecordings[index].current === true) {
					this.sfRecordings[index].current = false
				} else {
					this.sfRecordings[index].current = true
				}
			}
	    }
	}
</script>

<style rel="stylesheet" style="stylesheet/scss" lang="scss">
	.m-wrapper{
		.title{
			.list{
				margin-top:6px;
				font-size:14px;
				.back{
					color:#ffb372;
				}
			}	
		}
		.m-table{
			height: 563px;
			margin-top: 19px;
			ul{
				min-height:100%;
				font-size:0;
				li{
					position:relative;
					display:inline-block;
					margin-top:56px;
					margin-right:80px;
					.u-title{
						font-size:16px;
						color:#2b2b2b;
					}
					.u-input{
						margin-top:10px;
						&.selected{
							background:#ffffff;
							border:1px solid #e6e6e6;
							box-shadow:0 4px 16px 0 rgba(0,0,0,0.20);
							border-radius:4px;
							
						}
					}
					.icon-choose{
						position:absolute;
						top:44px;
						right:9px;
					}
					.ic-Wipeoff{
						position:absolute;
						top:40px;
						right:9px;
						cursor:pointer;
					}
				}	
			}
			.m-bottom{
				text-align: right;
				width:calc( 100% -  80px );
				line-height:87px;
				margin:-87px auto 0 auto;
				border-top:1px solid #eaeaea;
				.save{
					margin-right:20px;
					padding:6px 74px;
				}
				.filling{
					padding:6px 30px;
				}
			}
		}
		
	}
	.dialog-wrapper{
		position:fixed;
		z-index: 100;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background:rgba(0,0,0,0.30);
		transition:all .3s;
		&.fade-enter, &.fade-leave-active{
				opacity:0;
				background:rgba(7,17,27,0);
			}
		.m-dialog{
			position:fixed;
			top:50%;
			left:50%;
			z-index:101;
			width:440px;
			height:560px;
			border-radius:10px;
			background:#fff;
			transform: translateX(-50%) translateY(-50%);
			.header{
				line-height:60px;
				padding:0 20px;
				font-size:18px;
				color:#333;
				border-bottom:1px solid #eaeaea;
				.close{
					float:right;
					margin-top:20px;
					cursor:pointer;
				} 
			}
			.m-select{
				position:relative;
				padding:13px 20px;
				select{
					width:398px;
					height:39px;
					padding:0 11px;
					font-size:16px;
					color:#ffb372;
					border:1px solid #e6e6e6;
					border-radius:4px;
					background:#f6f6f6;
					box-sizing:border-box;
					appearance:none;
				    -moz-appearance:none;
				    -webkit-appearance:none;
				}
				.u-triangle{
					position:absolute;
					right:41px;
					top:29px;
				}
			}
			.m-content{
				width:400px;
				height:330px;
				margin:12px auto;
				font-size:16px;
				color:#333;
				overflow:auto;
				.list-item{
					position:relative;
					margin:0 0 8px 0;
					padding:0 19px;
					line-height:40px;
					&:hover{
						background:#f6f6f6;
					}
					.item-selected{
						position:absolute;
						right:20px;
						top:14px;
					}
				}
			}
			.m-bottom{
				line-height:78px;
				text-align:center;
				border-top:1px solid #eaeaea;
				.btn-ok{
					padding:6px 75px; 
				}
			}
		}	
	}
</style>
