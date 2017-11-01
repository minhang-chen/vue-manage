<template>
	<div>
		<header-public></header-public>
		<div class="m-wrapper">
			<div class="title">
				<span>我的患者</span>
				<router-link to="/myInformation">
					<a href="javascript:;" class="btn-white"><img class="icon-person" src="../../images/ic_addperson.png" height="23" width="23">添加患者</a>
				</router-link>
			</div>
			<div class="m-table">
				<table class="table">
					<thead>
						<tr>
							<td>ID</td>
							<td>姓名</td>
							<td>年龄</td>
							<td>操作</td>
						</tr>
					</thead>
					<tbody>
						<tr v-for="(information, index) in informations">
							<td>{{information.id}}</td>
							<td>{{information.name}}</td>
							<td>{{information.age}}</td>
							<td>
								<div class="operating">
									<a href="javascript:;" class="xinxi"><img src="../../images/ic_xinxi.png" height="30" width="30"></a>
									<a href="javascript:;" calss="list"><img src="../../images/ic_list.png" height="30" width="30"></a>
									<a href="javascript:;" class="delet" @click="delet(index)"><img src="../../images/ic_delet.png" height="30" width="30"></a>
								</div>
							</td>
						</tr>
						<!-- <tr>
							<td>1234567</td>
							<td>美丽的神话</td>
							<td>39</td>
							<td>
								<div class="operating">
									<a href="javascript:;" class="xinxi"><img src="../../images/ic_xinxi.png" height="30" width="30"></a>
									<a href="javascript:;" calss="list"><img src="../../images/ic_list.png" height="30" width="30"></a>
									<a href="javascript:;" class="delet"><img src="../../images/ic_delet.png" height="30" width="30"></a>
								</div>
							</td>
						</tr> -->								
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

	export default{
		components: {
			'header-public': header
		},
		data () {
			return {
				informations: [{id: '阿斯顿发放', name: '啦啦啦', age: '39'}, {id: '暗示法第三方', name: '啦啦啦', age: '39'}, {id: '阿发', name: '啦啦啦', age: '39'}]
			}
		},
		methods: {
			delet: function(index) {
				this.informations.splice(index, 1)
			}
		}
	}
</script>

<style rel="stylesheet" style="stylesheet/scss" lang="scss">
	.m-wrapper{
		.title{
			overflow:hidden;
			.btn-white{
				position:relative;
				float:right;
				box-sizing:border-box;
				padding:8px 29px 8px 55px;
				.icon-person{
					position:absolute;
					top:7px;
					left:26px;
				}
			}
		}
		.m-table{
			height: 563px;
			margin-top: 39px;
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
