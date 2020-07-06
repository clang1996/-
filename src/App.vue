<template>
    <div id="app">
        <throttle/>
        <debounced/>
    </div>
</template>

<script>
	import Throttle from './components/throttle';
	import Debounced from './components/debounced';

	export default {
		components: {
			'throttle': Throttle,
			'debounced': Debounced,
		},
		name: 'App',
	};
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
