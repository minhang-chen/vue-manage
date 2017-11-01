<template>
	<div>
		<header-public></header-public>
		<div class="m-wrapper">
			<div class="title">
				<div>随访表</div>
				<div class="list">
					<a href="javascript:;" class="back">返回</a>
					<a href="javascript:;" class="list-item">我的患者</a>><a href="javascript:;" class="list-item">随访表</a>
					<div class="m-name">
						<span class="name">张小兰</span>（ID：<span>1234564</span>）
					</div>
				</div>
			</div>
			<div class="m-table">
				<div class="m-tr">
					<p class="title">1、饮食记录完整性如何？</p>
					<div style="display:flex">
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									完整 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									不完整
								</label>
							</div>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">2、具体饮食特色如何？</p>
					<div style="display:flex">
						<span class="u-name">主食</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									完整 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									不完整
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">蛋白质</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									过多 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									过少
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									正常 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									肉类为主
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									鸡鸭为主 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									鱼虾类为主
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									均衡 
								</label>
							</div>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">3、运动执行情况？</p>
					<div style="display:flex">
						<span class="u-name">有氧运动</span>

						<div class="question-box">
							<span class="u-name">类型</span>
							<div class="m-option">
								<input class="u-text" type="text">
							</div>
							<span class="u-name">时长</span>
							<div class="m-option">
								<input class="u-text" type="text">
								<span class="u-unit">分钟</span>
							</div>
							<span class="u-name">（建议30~60分钟）</span>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">抗阻力运动</span>

						<div class="question-box">
							<span class="u-name">类型</span>
							<div class="m-option">
								<input class="u-text" type="text">
							</div>
							<span class="u-name">时长</span>
							<div class="m-option">
								<input class="u-text" type="text">
								<span class="u-unit">分钟</span>
							</div>
							<span class="u-name">（建议每周3-5分钟，每次10分钟）</span>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">4、体重情况？</p>
					<div style="display:flex">
						<span class="u-name">是否每日称量体重（晨起称量）并记录体重？</span>

						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">本周体重下降</span>

						<div class="question-box">
							<div class="m-option">
								<input class="u-text" type="text">
								<span class="u-unit">公斤</span>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">体重下降速度过快或过慢？</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">5、用药依从性？</p>
					<div style="display:flex">
						<span class="u-name">是否有忘记服药经历？</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
							<div class="m-option">
								<input class="u-text" type="text">
								<span class="u-unit">公斤</span>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">是否曾自行停药？</span>

						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">6、不良反应</p>
					<div style="display:flex">
						<span class="u-name">低血糖反应及低血压的症状（心慌、大汗、黑朦）</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">低血压的症状（头晕、目眩、黑朦）</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">便秘</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">饥饿感</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
					<div style="display:flex">
						<span class="u-name">心理障碍</span>
						<div class="question-box">
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									是 
								</label>
							</div>
							<div class="m-option">
								<input class="u-radio" type="radio">
								<label class="hook">
									否 
								</label>
							</div>
						</div>
					</div>
				</div>
				<div class="m-tr">
					<p class="title">7、提醒1周后门诊就诊</p>
					<span class="remind-text">带饮料运动日记，不需要空腹</span>
				</div>
				<div class="m-tr">
					<p class="title">8、特殊情况备注</p>
					<textarea class="m-textarea" placeholder="请填写特殊情况">
						
					</textarea>
				</div>
				<div class="m-bottom">
					<a href="javascript:;" class="u-btn save">保存</a>
				</div>
			</div>
		</div>
		
	</div>
</template>

<script>
	import header from '../../components/header/header.vue'

	export default{
		components: {
			'header-public': header
		}
	}
</script>

<style rel="stylesheet" style="stylesheet/scss" lang="scss">
	.m-wrapper{
		padding-bottom:109px;
		.title{
			.list{
				margin-top:6px;
				font-size:14px;
				.back{
					color:#ffb372;
				}
				.m-name{
					float:right;
				}
			}	
		}
		.m-table{
			margin-top:19px;
			padding: 0 27px;
			.m-tr{
				font-size:0;
				border-bottom: 1px solid #eaeaea;
				.title{
					margin-top:26px;
					font-size:16px;
					color:#2b2b2b;
				}
			}
			.m-bottom{
				text-align: right;
				width:calc( 100% -  80px );
				line-height:87px;
				margin:0 auto 0 auto;
				.save{
					margin-right:20px;
					padding:6px 74px;
				}
			}
		}
	}	
</style>
