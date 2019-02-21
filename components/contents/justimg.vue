<template>
    <div>
        <v-card flat>
            <v-layout row>
                <div>
                    <v-card-title>
                    <div>
                        <v-img 
                        :src="config.img"
                        aspect-ratio=1
                        max-height="200px"
                        width="450px"
                        ></v-img>
                    </div>
                    </v-card-title>
                    <v-card-actions>
                        <p>Times are changin fast and while some of us were simply..</p>
                        <!-- <minidate style="color:blue" :config="config.minidate"></minidate> -->
                        <v-spacer></v-spacer>
                        <div>
                            <span><a href="">See More...</a></span>
                        </div>
                    </v-card-actions>
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
