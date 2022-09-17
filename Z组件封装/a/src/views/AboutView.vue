<template>
	<div class="about">
		<h1>This is an about page</h1>
		<vant-crads title="这是夏洛特" :des='aaa' pay='12' @comm='msg'>
			<div slot="tag">
				<span>{{mm}}</span>
			</div>
		</vant-crads>
	</div>
</template>
<script>
	import vantCrads from '../components/vantCrads.vue'
	export default{
		components:{
			vantCrads
		},
		data(){
			return{
				aaa:'这是喜剧片',
				mm:'没窗'
			}
		},
		methods:{
			msg(e){
				console.log(e);
			}
		}
	}
</script>