<template>
	<div class="container mx-auto p-4" style="background-color: black">
		<h1 class="text-4xl font-bold text-center mb-10">我们的产品</h1>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<ProductCard
				v-for="product in products"
				:key="product.id"
				:title="product.title"
				:description="product.description"
			/>
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
					title: '产品一',
					description: '这是产品的详细描述，介绍产品的功能和特点。'
				},
				{
					id: 2,
					title: '产品二',
					description: '这是产品的详细描述，介绍产品的功能和特点。'
				},
				{
					id: 3,
					title: '产品三',
					description: '这是产品的详细描述，介绍产品的功能和特点。'
				}
			]
		}
	}
}
</script>
