<template>
	<view class="content">
		<pickerAddress @change="change">{{txt}}</pickerAddress>
	</view>
</template>

<script>
	import pickerAddress from '../../components/wangding-pickerAddress/wangding-pickerAddress.vue'
	export default {
		components:{
			pickerAddress
		},
		data() {
			return {
				txt: '选择地址',
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			change(data) {
				this.txt = data.data.join('')
				console.log(data.data.join(''))
			}
		}
	}
</script>
