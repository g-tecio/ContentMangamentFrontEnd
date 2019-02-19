<template>
    <div>
        <v-card flat>
            <v-layout row>
                <div>
                    <v-card-title>
                        <v-layout column>
                            <div class="headline">
                                {{config.title}} 
                            </div>
                            <br>
                            <div><dates :config="config.dates"></dates></div>
                            <br>
                            <div>{{config.content}}</div>
                        </v-layout>
                    </v-card-title>
                    <v-card-actions>
                        <minidate style="color:blue" :config="config.minidate"></minidate>
                        <v-spacer></v-spacer>
                        <div>
                            <span><a href="">ver mas...</a></span>
                        </div>
                    </v-card-actions>
                </div>
                <div>
                    <v-img 
                    :src="config.img"
                    aspect-ratio=1
                    max-height="300px"
                    width="250px"
                    ></v-img>
                </div>
                <slot name="line"></slot>
            </v-layout>
        </v-card>
    </div>
</template>

<script>
import dates from '~/components/dates'
import minidate from '~/components/minidate'

export default {
    props:['config'],
    components:{
        dates,
        minidate
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
