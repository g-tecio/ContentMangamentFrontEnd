<template>
	<div>
		<v-layout align-center justify-center column >
			<TodayDate class="complete-width font_cutive"></TodayDate>
			<br>
			<optionmenu class="complete-width font_cutive" :config="option_Menu" ></optionmenu>
		</v-layout>
		<div>
			<info-content class="font_cutive"></info-content>
		</div>
		<hr style="margin-bottom:10px">
		<hr>
		<br>
		<v-layout row >
			<v-flex xs9>
				<v-layout>
					<newsbody></newsbody>
				</v-layout>
			</v-flex>
			<v-flex xs3>
				<mininews :config="mininews"></mininews>
			</v-flex>
		</v-layout>
		<hr>
		<br>
        <v-layout>
			<v-flex>
				<newsfooter></newsfooter>
			</v-flex>
		</v-layout>
		<br>
		<hr>
		<br>
		<newsbottom></newsbottom>
	</div>
</template>

<script>
import optionmenu from '~/components/navbar/optionmenu'
import TodayDate from '~/components/TodayDate'
import ligthbar from '~/components/navbar/ligthbar'
import infoContent from '~/components/infoContent'
import newsbody from '~/components/newsbody'
import mininews from '~/components/mininews'
import newsfooter from '~/components/newsfooter'
import newsbottom from '~/components/newsbottom'
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
                    dates: {
						words: '438 words',
						date: 'Jan 2019'
					}
                },
                {
                    title: 'Easy One head line',
                   	dates:{ 
						words: '438 words',
						date: 'Jan 2019'
					}
                },
                {
                    title: 'Easy One head line',
                    dates:{
						words: '438 words',
						date: 'Jan 2019'
					}
                },
                {
                    title: 'Easy One head line',
                    dates:{
						words: '438 words',
						date: 'Jan 2019'
					}
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
		newsbody,
		mininews,
		newsfooter,
		newsbottom
	}
}
</script>
<style lang="stylus">
	.complete-width
		width 100%
	.font_cutive
		font-family: 'Cutive'
</style>
