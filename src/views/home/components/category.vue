<script setup>
defineProps({
   kinds: {
		 type: Array,
		 default: () => ([]),
	 }
})
</script>

<template>
	<div class="container">
		<template v-for="(item, index) in kinds" :key="index">
			<div class="item">
				<div class="album">
					<img :src="item?.pictureUrl" alt=""/>
				</div>
				<div class="title">
					{{ item?.title }}
				</div>
			</div>
		</template>
	</div>
</template>

<style scoped lang="less">
.container {
	display: flex;
	flex-shrink: 0;
	justify-content: space-evenly;
	overflow-x: scroll;

	.item {
		text-align: center;
		padding: 0 5vw  /* 10/3.75 */;
		.album{
			img{
				width: 8vw  /* 30/3.75 */;
			}
		}
		.title {
			white-space: nowrap;
			font-size:0.53vw  /* 2/3.75 */;
		}
	}

}
</style>