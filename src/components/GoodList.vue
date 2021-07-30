<template>
	<div name="show">
		<ul class="goodlist">
			<li v-for="good in list">
				<img v-bind:src="good.img">
				<p>{{good.goodName}}</p>
			</li>
		</ul>
	</div>
</template>
<script type="text/javascript">
	export default{
		name:"show",
		data(){
			var obj=this;
			var url="";
			if(obj.goodId==1){
				url="json/bjb.json"
			}else if(obj.goodId==2){
				url="json/sj.json"
			}else{
				url="json/bjb.json"
			}
			this.$http.get(url).then(function(res){
					obj.list=res.data
			})
			return{
				list:[]
			}
		},
		props:{//父组件传值通过props接收
			goodId:Number
		},
		watch:{
			goodId(){
				var obj=this;
				var url="";
				if(obj.goodId==1){
					url="json/bjb.json"
				}else if(obj.goodId==2){
					url="json/sj.json"
				}else{
					url="json/bjb.json"
				}
				this.$http.get(url).then(function(res){
					obj.list=res.data
				})
				return{
					list:[]
				}
			}
		}
	}
</script>
<style>
	.goodlist li{
		width: 200px;
		height: 200px;
		float: left;
		font-size: 12px;
		color: red;
		margin-bottom: 10px;
	}
	.goodlist img{
		width:180px;
		height:180px;
	}
</style>