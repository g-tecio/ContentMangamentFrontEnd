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
        <newsheader :config="item"/>
        <v-layout>
            <v-flex md9>
                <v-layout column>
                    <div>
                        <p>{{text1}}</p>
                        <p>{{text2}}</p>
                        <p>{{text3}}</p>
                        <p>{{text1}}</p>
                        <p>{{text2}}</p>
                    </div>
                    <v-layout row>
                        <v-flex md6> <justtitle :config="item"/> </v-flex>
                        <v-flex md6> <c-content :config="item"/> </v-flex>
                    </v-layout>
                </v-layout>
            </v-flex>
            <v-flex md3>
                <v-layout column>
                    <mininews :config="mininews"/>
                    <c-content3 style="padding:10px" :config="item"/>
                </v-layout>
            </v-flex>
        </v-layout>
        
    </div>
</template>

<script>
import optionmenu from '~/components/navbar/optionmenu'
import TodayDate from '~/components/TodayDate'
import infoContent from '~/components/infoContent'
import mininews from '~/components/mininews'

import justtitle from '~/components/contents/justtitle'
import content1 from '~/components/contents/content1'
import content3 from '~/components/contents/content3'
import newsheader from '~/components/contents/newsheader'
export default {
    data(){
        return{
            item:{
                img:'http://www.pcb.ub.edu/portal/image/journal/article?img_id=1412237&t=1517312061634',
                title:'This Module is an intro to the full article',
                dates:{words:'423 words',date:'Jan 2019'}, 
                content:'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not',
                minidate:'Tuesday, February 12'
            },
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
            text1:`Loren mumps dolor sit mate, detract misstates in per. Eu wist intelligent tied, acquit per sues rip ides emu in. Minim interpretations man en. Cu mutate repudiate ed, dictum ermines underused mam ea. Nam e quad qua eke, re me sues om ques men nadir. E professed asseverate em, diam elaborate delicateness cum id. Dolor unique id has. Ea an definiteness dissents dissident, ileum labor ram it. Us doctors time am error ibis no. Imus en elite scripts occurrence. Visa re quid recuse, in decor asseverate disciplining viz. I man quad exercise, populous possum instructor in me.`,
            text2:`Ad ram leis lucid lies, in quo dis risque civics cum, re consul sol eat usu. Merriam perpetual occurrence est at, per vitae. Est en aim occurrence persecute in, males deterministic e sea. Val ea ques elite. Requiem effendi an viz, sequel rill animal ea has, ad prob option integer ea. No grace descriptor per, passim qua we discern an sea. Quandary marchioness quo wt, ea sapper mastitis duo, ea quango solute viz. Dec ore offend it man re, est no dolor es explicate, re dicta elect ram demo critic duo. Ala emus no duo, obi verier ed an. Hui avidity kumquat in. Gypsum dissed effendi id me, est ad erred grace officious.`,
            text3:`Gracie nominal id xiv. I onset voluminous eons, pro mutate passim ex. Ermine squeal interpretative cu quo, est era fellas. Eu wist intelligent tied, acquit per sues rip ides emu in. Vela id brute dolor um peen chum. Unitarian elect ram patriot, en sea tuber gen constitute, rebus illus adolescents sit. Ill um deselect ma ad, en ferric patine sentient vim. Risque croquet pro ea. Est ea chin ma rum momentum.`,
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
    components:{
        optionmenu,
        TodayDate,
        infoContent,
        mininews,
        justtitle,
        'c-content': content1,
        'c-content3': content3,
        newsheader
    },
    methods:{
    }
}
</script>

<style lang="stylus">
	.complete-width
		width 100%
	.font_cutive
		font-family: 'Cutive'

</style>
