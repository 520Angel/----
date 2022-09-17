<template>
	<div>
		<div class="card">
			<div class="card-img">
				<img src="../assets/logo.png" alt="">
			</div>
			<div class="card-des">
				<p>{{title}}</p>
				<p>{{des}}</p>
				<slot name="tag"></slot>
				<p @click="chuan">{{pay}}</p>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				msg:'aaa'
			}
		},
		props:{
			title:{
				type:String,
				default:'这是电影'
			},
			des:{
				type:String,
				default:''
			},
			pay:{
				type:String,
				default:''
			}
		},
		methods:{
			chuan(){
				this.$emit('comm',this.msg)
			}
		}
	}
</script>

<style>
	.card{
		display: flex;
	}
	.card-img{
		width: 40%;
	}
	.card-img img{
		width: 100%;
	}
	.card-des{
		flex: 1;
		text-align: left;
	}
</style>
