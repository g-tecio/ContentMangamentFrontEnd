<template>
    <v-layout row>
        <v-flex md9 >
            <v-layout justify-center column>
                <v-flex xs12>
                    <v-layout align-center row wrap>
                        <v-flex md6 sm12 xs12>
                            <content2 :config="item">
                                <div slot="line" class="linevnf"></div>
                            </content2>
                        </v-flex>
                        <v-flex md3 sm6 xs12>
                            <content2 :config="item">
                                <div slot="line" class="linevnf"></div>
                            </content2>
                        </v-flex>
                        <v-flex md3 sm6 xs12>
                            <content2 :config="item"></content2>
                        </v-flex>
                    </v-layout>
                </v-flex>
                <hr style="margin-top:5px; margin-bottom:10px;">
                <v-flex>
                    <v-layout align-center justify-center>
                        <v-flex>
                            <content1 :config="item"></content1>
                        </v-flex>
                    </v-layout>
                </v-flex>
            </v-layout>
        </v-flex>
        <div class="linevp"></div>
        <v-flex style="max-width: 300px">
            <v-layout  justify-center  column>
                <v-flex>
                    <content3 :config="item"></content3>
                </v-flex>
                <v-flex>
                    <content3 :config="item"/>
                </v-flex>
            </v-layout>
        </v-flex>
    </v-layout>
</template>

<script>
import content1 from '~/components/contents/content1'
import content2 from '~/components/contents/content2'
import content3 from '~/components/contents/content3'
export default {
    data(){
        return{
            item: {
                    img:'http://www.pcb.ub.edu/portal/image/journal/article?img_id=1412237&t=1517312061634',
                    title:'This Module is an intro to the full article',
                    dates:{words:'423 words',date:'Jan 2019'}, 
                    content:'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not',
                    minidate:'Tuesday, February 12'
                },
        }
    },
    components:{
        content1,
        content2,
        content3
    }

}
</script>

<style lang="stylus">
    .linevp
        background black
        width 1px
        min-height 100%
        border-color black
        margin 10px
    .linevnf
        background black
        width 1px
        height 250px
        border-color black
        margin-right 1px
</style>
