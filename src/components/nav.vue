<template>
	<div class="nav_container">
		<div class="menu">
			<el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect" :active-text-color="activeColor" router menu-trigger="hover">
			  <el-menu-item :index="erp_nav.erpmain.url">{{erp_nav.erpmain.name}}</el-menu-item>
				<el-submenu index="2">
			    <template slot="title">{{erp_nav.nowpage}}</template>
			    <el-submenu v-for="i in erp_nav.children" :index="i.url">
			      <template slot="title">{{i.name}}</template>
			      <el-menu-item v-for="j in i.children" :index="j.url">{{j.name}}</el-menu-item>
			    </el-submenu>
			  </el-submenu>
			</el-menu>
			<div class="line"></div> 
		</div> 
	</div>
</template>

<script>
export default {
	name: 'sd-nav',
  	data () {
	    return {
	    activeColor:'#9b1700',
	    activeIndex: 'erpmain',
        erp_nav:{
        	nowpage:"导航",
        	erpmain:{
        		name:"首页",
        		url:"erpmain"
        	},
        	children:[{
        		name:"采购系统",
        		url:"cgxt",
        		children:[
	        	{
	        		name:"采购开单",
	        		url:"cgkd"
	        	},
	        	{
	        		name:"采购订单",
	        		url:"cgdd"
	        	}]
	        },
        	{
        		name:"销售系统",
        		url:"xsxt",
        		children:[{
        		name:"销售开单",
        		url:"xskd"
	        	},
	        	{
	        		name:"销售订单",
	        		url:"xsdd"
	        	}]
        	}]
        }
      };
	},
    methods: {
      handleSelect(key, keyPath) {

      }
    }
}
</script>
<style lang="less">
	@import '../style/mixin';
	.el-cascader{
		line-height: 60px;
	}
</style>