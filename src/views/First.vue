<template>
	<div class="main">
		<div class="left">
			<Left></Left>
		</div>
		<div class="right">
			<div class="top">
				<img src="../../public/img/title.jpg">
			</div>
			<div class="bottom">
				<Right></Right>
			</div>
		</div>
	</div>
</template>
<script type="text/javascript">
	import Left from "../components/Left.vue"
	import Right from "../components/Right.vue"
	export default{
		components:{
			Left,
			Right
		}
	}
</script>
<style type="text/css">
	*{
		margin: 0px;
		padding: 0px;
	}
	.left{
		width: 100px;
		margin-right: 10px;
		float: left;
	}
	.right{
		width: 1000px;
		float: left;
		margin-left: 10px;
	}
	.main{
		width:1200px;
		margin: 20px auto;
	}
	.top img{
		height: 200px;
		width: 1000px;
	}
	.left,.right{
		background-color: #f5f5f5;
		height: 500px;
	}
</style>