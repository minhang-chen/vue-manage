<template>
	<div class="pagination">
		<span class="page-btn" v-if="total">共{{total}}条消息记录</span>
		<span class="icon page-btn" :class="{'z-disabled': isFirst}"@click="toFirst"><i class="iconfont icon-diyiye"></i></span>
		<span class="icon page-btn" :class="{'z-disabled': isFirst}"@click="pre"><i class="iconfont icon-shangyiye"></i></span>
		<span class="icon page-btn" :class="{'z-disabled': isLast}" @click="next"><i class="iconfont icon-xiayiye"></i></span>
		<span class="icon page-btn" :class="{'z-disabled': isLast}" @click="toLast"><i class="iconfont icon-zuihouyiye"></i></span>
	</div>
</template>

<script type="text/ecmascript-6"></script>

<style rel="stylesheet">
	
</style>
