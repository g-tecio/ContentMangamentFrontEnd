<template>
    <!-- <div> -->
        <v-layout row fill-height>
            <v-flex xs12 v-for="item in items" :key="item">
                <v-card flat>
                  <v-layout row>
                        <div>
                            <v-card-title>
                                <v-layout column>
                                    <div class="headline">
                                        {{item.title}} 
                                    </div>
                                    <br>
                                    <div><dates :config="item.dates"></dates></div>
                                    <br>
                                    <div>{{item.content}}</div>
                                </v-layout>
                            </v-card-title>
                            <v-card-actions>
                                <minidate style="color:blue" :config="item.minidate"></minidate>
                                <v-spacer></v-spacer>
                                <div>
                                    <span>ver mas...</span>
                                </div>
                            </v-card-actions>
                        </div>
                        <div>
                            <v-img 
                            :src="item.img"
                            aspect-ratio=1
                            max-height="300px"
                            width="250px"
                            ></v-img>
                        </div>
                        <div class="linevnf"></div>
                  </v-layout>
                </v-card>
            </v-flex>
        </v-layout>
    <!-- </div> -->
</template>

<script>
import minidate from '~/components/minidate'
import dates from '~/components/dates'
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
        minidate,
        dates
    }
}
</script>

<style lang="stylus">
    .linevnf
        background black
        width 1px
        height 250px
        border-width 1px
        border-color black
        margin 15px
</style>
