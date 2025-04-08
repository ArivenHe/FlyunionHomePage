<script>
export default {
	name: "Footer",
	methods: {
		goto() {
			window.location.href='http://beian.miit.gov.cn'
		}
	}
}
</script>

<template>
	<div style="width:100%;height:11%;padding-left: 30px" class="	base-100">
		<div class="copyright"> Copyright &copy; 2025 Flyunion Studio. All Rights Reserved <br>
			<p @click="goto">蜀ICP备2021007446号-4-1</p>
		</div>
		<br>
	</div>
</template>

<style scoped>

</style>