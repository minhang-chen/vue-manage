<template>
	<div>
		<header-public></header-public>
		<div class="m-wrapper">
			<div class="title">
				<div>我的患者</div>
				<div class="list">
					<a href="javascript:;" class="back">返回</a>
					<a href="javascript:;" class="list-item">我的患者</a>><a href="javascript:;" class="list-item">个人信息</a>
					<div class="m-name">
						<span class="name">张小兰</span>（ID：<span>1234564</span>）
					</div>
				</div>
			</div>
			<div class="m-table">
				<table class="table">
					<thead>
						<tr>
							<td>随访表名称</td>
							<td>操作</td>
						</tr>
					</thead>
					<tbody>
						<tr v-for="(sfName, index) in sfNames">
							<td>{{sfName}}</td>
							<td>
								<div class="operating">
									<a href="javascript:;" class="xinxi"><img src="../../images/ic_bianji.png" height="30" width="30"></a>
									<a href="javascript:;" class="delet" @click="delet(index)"><img src="../../images/ic_delet.png" height="30" width="30"></a>
								</div>
							</td>
						</tr>
						<!-- <tr>
							<td>体重管理-第一周电话随访记录</td>
							<td>
								<div class="operating">
									<a href="javascript:;" class="xinxi"><img src="../../images/ic_bianji.png" height="30" width="30"></a>
									<a href="javascript:;" class="delet"><img src="../../images/ic_delet.png" height="30" width="30"></a>
								</div>
							</td>
						</tr>	 -->
					</tbody>
				</table>
				<div>
					
				</div>
			</div>
		</div>
	</div>
</template>
	
<script>
	import header from '../../components/header/header.vue'

	export default {
		components: {
			'header-public': header
		},
		data () {
			return {
				sfNames: ['体重管理-第一周电话随访记录', '体重管理-第一周电话随访记录']
			}
		},
		methods: {
			delet: function(index) {
				this.sfNames.splice(index, 1)
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
				.m-name{
					float:right;
				}
			}	
		}
		.m-table{
			height: 563px;
			margin-top: 19px;
			.table{
				.operating{
					position:absolute;
					left:61px;
					top:10px;
					font-size:0;
					a{
						margin-right:13px;
					}
				}
			}
		}
	}
</style>
