<template>
	<div>
		<div v-if="kk==1">
			<GoodList :goodId="1"></GoodList>
		</div>
		<div v-else-if="kk==2">
			<GoodList :goodId="2"></GoodList>
		</div>
		<div v-else-if="kk==3">
			333333
		</div>
		<div v-else>
			<GoodList :goodId="0"></GoodList>
		</div>
		</div>
	</div>
</template>
<script type="text/javascript">
	import Msg from "./msg.js"
	import GoodList from "./GoodList.vue"
	export default{
		data(){
			return{
				kk:0
			}
		},
		mounted:function(){
			var _this=this;
			Msg.$on("val",function(e){
					_this.kk=e
			})
		},
		components:{
			GoodList
		}
	}
</script>
