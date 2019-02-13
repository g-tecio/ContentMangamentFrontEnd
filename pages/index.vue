<template>
	<div>
		<v-layout align-center justify-center column >
			<TodayDate class="complete-width"></TodayDate>
			<br>
			<optionmenu class="complete-width" :config="option_Menu" ></optionmenu>
		</v-layout>
		<div>
			<info-content></info-content>
		</div>
		<hr>
		<br>
		<hr>
	</div>
</template>

<script>
import optionmenu from '~/components/navbar/optionmenu'
import TodayDate from '~/components/TodayDate'
import ligthbar from '~/components/navbar/ligthbar'
import infoContent from '~/components/infoContent'
export default {
	data(){
		return{
			option_Menu:[
                'World',
                'Politics',
                'Business',
                'Opinion',
                'Tech',
                'Sience',
                'Health',
                'Sports',
                'Arts',
                'Books',
                'Style',
                'Food',
                'Travel',
                'Magazine'
            ]}
	},
	methods:{
	},
	components:{
		optionmenu,
		TodayDate,
		ligthbar,
		'info-content': infoContent
	}
}
</script>
<style lang="stylus">
	.complete-width
		width 100%
</style>
