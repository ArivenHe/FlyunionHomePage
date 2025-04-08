<template>
	<div class="hero bg-base-200 min-h-screen">

		<div class="hero-content flex-col lg:flex-row-reverse">
			<div class="people-list">
				<h1  class="text-5xl font-bold custom-letter-spacing gradient-text mb-8 gradient-text">更多产品</h1>
				<br>
				<div class="cards-container">
					<div class="grid grid-cols-1 md:grid-cols-4 gap-6">
						<ProductCard
							v-for="product in products"
							:key="product.id"
							:title="product.title"
							:description="product.description"
						/>
					</div>
				</div>
			</div>

		</div>
	</div>
</template>

<script>
import ProductCard from './ProductCard.vue'

export default {
	components: {
		ProductCard
	},
	data() {
		return {
			products: [
				{
					id: 1,
					title: 'AirAmaz-Fsd™',
					description: '新一代高性能联飞网络解决方案'
				},
				{
					id: 1,
					title: 'AirAmaz-Audio™',
					description: '新一代高性能模拟飞行机载调频软件'
				},
				{
					id: 3,
					title: 'Flyunion',
					description: '新一代飞行电子包(八月推出首个版本)'
				},
				{
					id: 4,
					title: 'Flyunion-VA',
					description: '新一代虚拟航司系统(未发布)'
				}
			]
		}
	}
}
</script>
<style>
.gradient-text {
	background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}
</style>