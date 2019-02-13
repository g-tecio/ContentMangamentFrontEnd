<template>
    <div>
        <v-layout row align-center justify-center fill-height>
            <v-flex xs4 v-for="item in news" :key="item">
                <v-layout row align-center justify-center fill-height>
                   <v-card flat style="width:100%" class="black--text">
                    <v-layout>
                        <v-flex xs5>
                        <v-img
                            :src="item.img"
                            aspect-ratio=1.3
                            max-width="250px"
                            contain
                        ></v-img>
                        </v-flex>
                        <v-flex xs7>
                        <v-card-title primary-title>
                            <div>
                                <div class="headline">{{item.title}}</div>
                                <div>{{item.content}}</div>
                            </div>
                        </v-card-title>
                        </v-flex>
                    </v-layout>
                    </v-card>
                <div class="linev"></div>
                </v-layout>
            </v-flex>
            <v-flex>
                <v-layout align-center justify-center fill-height>
                    <p>Money</p>
                </v-layout>
            </v-flex>
            <div class="linev"></div>
            <v-flex> 
                <v-layout align-center justify-center fill-height>
                    <p>weather</p>
                </v-layout>    
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
export default {
    data(){
        return{
            news:[
                {img:'https://www.ara.cat/2012/07/22/societat/cientific-laboratori-THINKSTOCK_741535932_11937986_900x600.jpg',title:'Times are changing fast...', content:'and whilist some of us were simply born into this meteoric times there are others who were not'},
                {img:'https://www.viaempresa.cat/uploads/s1/18/33/53/laboratori-cientific-120269_11_640x380.jpg',title:'Times are changing fast...', content:'and whilist some of us were simply born into this meteoric times there are others who were not'}
            ]
        }
    }
}
</script>

<style lang="stylus">
.linev
    background black
    width 3px
    height 100px
    border-width 10px
    border-color black
    margin-right 15px
</style>
