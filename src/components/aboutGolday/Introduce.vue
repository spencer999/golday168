<template>
	<div class="introduce">
		<!-- <section class="container">
			<video class="video" poster="./img/video.jpg" controls src="http://1251587264.vod2.myqcloud.com/4ad8a7d0vodtransgzp1251587264/e3bddfc99031868222975253471/f0.f30.mp4"></video>
			<p class="conText"> 香港金盛贵金属有限公司（以下简称为“金盛贵金属”）注册成立于香港，作为香港金银业贸易场认可的专业电子交易商，金盛贵金属致力为广大投资者打造优质可靠的贵金属投资服务平台。</p>
		      		<p class="conText">金盛贵金属(www.golday.com)是香港金银业贸易场AA类会员第047号行员，随着百年历史的香港金银业贸易场认可的电子交易商。单笔交易0.1手以上均提供「交易编码」，有据可查，保证所有交易公开透明。</p>
		</section> -->

		<section class="container" v-for="(item,index) in conList" :key="index">
			<!-- <h3 class="conTitle">{{item.tag}}</h3> -->
			<p class="conText">{{item.desc}}</p>
		</section> 

		<section class="container">
			<h3 class="titleC">全方位客户服务体系</h3>
			<app-advantage></app-advantage> 
		</section>
	</div> 
</template>

<script>
import advantage from './components/Advantage'
export default {
	name: 'introduce', 
	data () {
	    return {
	    	conList:[
	    		{  
	    			desc:"金盛盈富-金盛盈富投资有限公司（以下称“金盛盈富”），英文名GOLDAY HARVEST INVESTMENT LIMITED，隶属于香港金盛金融集团，为金盛金融集团旗下贵金属投资平台。从事伦敦金/银、99金、港币公斤条、人民币公斤条交易。",
	    		},
	    		{  
	    			desc:"金盛盈富致力为投资者提供「公平、公正、透明」的交易环境，不仅采用国际上先进的MT4&MF交易双平台，更震撼推出高于行业平均水平的伦敦金/银点差优惠活动，交易零佣金，使得投资者能够以最低成本获取最大投资回报。",
	    		},
	    		{ 
	    			desc:"金盛金融集团拥有严格的美国NFA牌照，是香港金银业贸易场047号行员。其旗下盈富公司所有交易活动也均受国际监管和严格符合香港法律标准。 ",
	    		},{  
	    			desc:" 金盛盈富的发展规划建立在在高度严谨及自律的营运准则上，将客户个人资金与公司的营运资金分开存放，提高客户资金存放的透明度，存款和取款都在香港持牌银行进行。更外聘专业核数师定期查核财务状况，再向管理层及相关机构呈交报告，以达至有效和谨慎的公司管理，让客户资金得到多重监控。",
	    		},{  
	    			desc:"金盛盈富汇集业内顶尖分析师、IT工程师、精算师、会计师、产品架构师、品牌运营及互联网营销领域的优秀人才，以集团化运营模式为全球投资者打造最为专业的贵金属投资服务平台，通过优质的客户服务，领先的平台技术，极具竞争力的交易成本，满足国内及国际投资者的不同需求。 ",
	    		},{  
	    			desc:"此外，金盛盈富始终坚持「以客户利益」为首位，客服团队全天24小时在线，提供一站式全方位的专业服务，随时为客户解答疑难，入金即时到账，保证取款2小时到账，让客户专尊享到最优质的贵金属投资服务，助力每一位投资者实现财富快速增值。 ",
	    		},  
	    	]
	    }
  	},
  	components:{
  		"app-advantage":advantage
  	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped> 	
	.video{
		width:100%;
		z-index:1;
	} 
	.titleC{
		font-size: 0.3rem; 
		color: #000;
		text-align: center;  
	}
</style>
