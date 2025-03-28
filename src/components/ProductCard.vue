<template>
	<div class="card bg-base-100 shadow-xl " >
		<div class="card-body">
			<h2 class="card-title">{{ title }}</h2>
			<p>{{ description }}</p>
			<div class="card-actions justify-end">
				<button class="btn btn-primary">了解更多</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		title: {
			type: String,
			required: true
		},
		description: {
			type: String,
			required: true
		}
	}
}
</script>
