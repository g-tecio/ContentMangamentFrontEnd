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
		<v-layout row >
			<v-flex xs9>
				<v-layot></v-layot>
			</v-flex>
			<v-flex xs3>
				<mininews :config="mininews"></mininews>
			</v-flex>
		</v-layout>
	</div>
</template>

<script>
import optionmenu from '~/components/navbar/optionmenu'
import TodayDate from '~/components/TodayDate'
import ligthbar from '~/components/navbar/ligthbar'
import infoContent from '~/components/infoContent'
import mininews from '~/components/mininews'
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
			],
			mininews:[
                {
                    title: 'Easy One head line',
                    words: '438 words',
                    date: 'Jan 2019'
                },
                {
                    title: 'Easy One head line',
                    words: '438 words',
                    date: 'Jan 2019'
                },
                {
                    title: 'Easy One head line',
                    words: '438 words',
                    date: 'Jan 2019'
                },
                {
                    title: 'Easy One head line',
                    words: '438 words',
                    date: 'Jan 2019'
                }
            ]
		}
	},
	methods:{
	},
	components:{
		optionmenu,
		TodayDate,
		ligthbar,
		'info-content': infoContent,
		mininews
	}
}
</script>
<style lang="stylus">
	.complete-width
		width 100%
</style>
