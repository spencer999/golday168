<template>
	<div class="contact">
		<div class="container">
			<img class="w100" src="./img/contact1.png" alt=""> 
			<p class="p1">地址：香港中环皇后大道222号启煌商业大厦2楼02室</p>
			<p class="p1">电话：+852 37582889</p>
			<p class="p1">Email：cs@golday168.com</p>
			<p class="p1">QQ：800063340</p>
			<p class="p1">网址 : https://m.golday168.com</p> 
			<!-- <div class="flex">
				<div class="wx">
					<img src="./img/contact2.jpg" alt=""> 
					<p class="p2">官方订阅号：goldayhk<br>独家黄金白银投分析</p>
				</div>
				<div class="wx"> 
					<img src="./img/contact3.jpg" alt=""> 
					<p class="p2">24小时客服：goldaycs<br>为投资者提供账户查询</p>
				</div>
			</div> -->
		</div>
	</div> 
</template>





<script>
export default {
	name: 'contact',
  	data () {
	    return {
	    	msg: 'Welcome to Your Vue.js App'
	    }
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped> 
	.w100{
		width:100%;
		display:block;
		margin-bottom:.25rem;
	}
	.p1{
		font-size: .30rem; 
		line-height: .48rem;  
	}
	.p2{
		font-size: .26rem; 
		line-height: .3rem; 
		word-break: break-all;
		text-align: center;
	}
	.flex{
		margin-top:.4rem;
		padding:0 .5rem;
	}
	.wx{
		width:2.8rem;
		text-align: center;
	}
	.flex img{
		width:2.14rem;
		height:2.1rem;
		margin:0 auto .15rem;
		display:block;
	}
</style>
