<template>
    <div>
        <button @click="click">防抖</button>
    </div>
</template>

<script>
	export default {
		data () {
			return {timeId: null};
		},
		methods: {
			click () {
				if (this.timeId) {
					window.clearTimeout(this.timeId);
				}
				this.timeId=setTimeout(
					() => {
						this.fn();
						this.timeId=null;
					}, 1000);
			},
			fn () {
				console.log('我执行了');
			},
		},
	};
</script>

<style lang="scss" scoped>

</style>