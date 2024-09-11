<template>
	<view>
		<button @click="open">打开选择器</button>
		<KDatePicker v-model="show" type="day" is-range @change="getDate" formatter="YYYY-MM-DD" />
    {{date}}
	</view>
</template>

<script>
	import KDatePicker from '../../components/k-date-picker/KDatePicker.vue'
	export default {
		components:{
			KDatePicker
		},
		data() {
			return {
				show: false,
        date: ''
			}
		},
		onLoad() {

		},
		methods: {
			open(){
				this.show = true
			},
      getDate(e){
        this.date = e
      }
		}
	}
</script>

<style>
</style>
