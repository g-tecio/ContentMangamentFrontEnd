<template>
    <!-- <div> -->
        <v-layout row wrap>
            <v-flex xs12 md6>
                <content1 :config="items[0]">
                    <div slot="line" class="linevnf"></div>
                </content1>
            </v-flex> 
            <v-flex xs12 md6>
                <content1 :config="items[1]"></content1>
            </v-flex>
        </v-layout>
    <!-- </div> -->
</template>

<script>
import content1 from '~/components/contents/content1'
export default {
    data(){
        return{
            items:[
                {
                    img:'http://www.pcb.ub.edu/portal/image/journal/article?img_id=1412237&t=1517312061634',
                    title:'This Module is an intro to the full article',
                    dates:{words:'423 words',date:'Jan 2019'}, 
                    content:'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not',
                    minidate:'Tuesday, February 12'
                },
                {
                    img:'http://www.pcb.ub.edu/portal/image/journal/article?img_id=1412237&t=1517312061634',
                    title:'This Module is an intro to the full article',
                    dates:{words:'423 words',date:'Jan 2019'}, 
                    content:'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not',
                    minidate:'Tuesday, February 12'
                },
            ]
        }
    },
    components:{
        content1
    }
}
</script>

<style lang="stylus">
    
</style>
