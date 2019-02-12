<template>
	<v-container>
		<v-layout align-center justify-center column class="text-xs-center">
			<br>
			<br>
			<v-img
			width="500px"
			height="90px"
			src="/img/banner2.jpg"></v-img>
			<TodayDate></TodayDate>
			<br>
			<optionmenu class="optionmenu" :config="optionmenu_props"></optionmenu>
		</v-layout>
	</v-container>
</template>

<script>
import optionmenu from '~/components/navbar/optionmenu'
import TodayDate from '~/components/TodayDate'
export default {
	data(){
		return{
			optionmenu_props:['Noticias', 'Cultura', 'Opinion', 'America Latina', 'Reposado']
		}
	},
	methods:{
	},
	components:{
		optionmenu,
		TodayDate
	}
}
</script>
<style lang="stylus">
	.optionmenu
		width 100%
</style>
