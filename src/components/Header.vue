<template>
	<div class="hello">
        
		<el-menu
			:default-active="activeIndex"
			class="el-menu-demo"
			mode="horizontal"
			@select="handleSelect"
			background-color="#545c64"
			text-color="#fff"
			active-text-color="#ffd04b"
            style="text-align:center;"
		>
            
			<el-menu-item >武器售卖专场</el-menu-item>
			<el-menu-item index="2">关于我们</el-menu-item>
            <el-menu-item index="3">新闻中心</el-menu-item>
		</el-menu>
	</div>
</template>

<script>
    export default {
        name: "Header",
        data() {
            return {
                activeIndex: "1",
            }
        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>