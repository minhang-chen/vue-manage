<template>
	<div class="m-header">
		<div class="m-logo">
			<img class="logo" src="../../images/logo2.png" height="39" width="97" >
		</div>
		<div class="m-search">
			<input type="text" placeholder="搜索" class="search">
			<img src="../../images/ic_search.png" class="img-search" height="13" width="13">
		</div>
	</div>
</template>

<script type="text/ecmascript-6"></script>

<style rel="stylesheet" style="stylesheet/scss" lang="scss">
	.m-header{
		overflow:hidden;
		font-size:0;
		background:#fff;
		box-shadow:0 2px 8px 0 rgba(189,189,189,0.29);
		.m-logo{
			float:left;
			width:203px;
			height:70px;
			line-height:70px;
			text-align:center;
			background-image:linear-gradient(-138deg, #ff9166 0%, #fbb78c 100%);
			.logo{
				display:inline-block;
				vertical-align:middle;
			}
		}
		.m-search{
			position:relative;
			float:right;
			margin-top:15px;
			margin-right:55px;
			.search{
				width:235px;
				line-height:38px;
				padding:0 16px;
				background:#f6f6f6;
				border:1px solid #e5e5e5;
				border-radius:18px;
				font-size:16px;
				color:#d3d3d3;
			}
			.img-search{
				position:absolute;
				top:13px;
				right:16px;
				cursor:pointer;
			}
		}
	}
</style>
