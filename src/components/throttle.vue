<template>
    <div>
        <button @click="click">节流</button>
    </div>
</template>

<script>
	export default {
		data () {
			return {cd: false};
		},
		methods: {
			click () {
				if (this.cd === false) {
					this.fn();
					this.cd=true;
					this.timeId();
				}
			},
			fn () {
				console.log('我执行了');
			},
			timeId () {
				setTimeout(() => {this.cd=false;}, 5000);
			}
		},
	};
</script>

<style lang="scss" scoped>

</style>