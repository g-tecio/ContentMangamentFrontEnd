<template>
    <div>
        <v-icon>reorder</v-icon>
        <v-layout class="" align-center justify-center row>
            <div style="margin-left: 30px"></div>
            <v-flex class="upper">
                <p>{{TodayDate}} </p>
            </v-flex>
            <v-spacer></v-spacer>
            <v-flex xs1 class="upper">
                <p>{{place}}</p>
            </v-flex>
        </v-layout>
        <v-flex>
            <div class="line"></div>
        </v-flex>
    </div>
</template>

<script>
export default {
    data(){
        return{
            TodayDate:'',
            place:'Durango, Dgo'
        }
    },
    mounted() {
        var meses = new Array ("January","February","March","April","May","June","July","August","September","October","November","Dicember");
        var diasSemana = new Array("Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday");
        var f=new Date();
        this.TodayDate = diasSemana[f.getDay()] + ", " + meses[f.getMonth()] + " " +f.getDate() +", " + f.getFullYear();
        this.place='Durango, Dgo'
        // this.$axios.get('api.openweathermap.org/data/2.5/weather?id=2172797').then((res)=>{
        //     debugger 
        //     this.weather = res
        // })
    },
}
</script>

<style lang="stylus">
    .line
        background black
        width 100%
        height 3px
        border-width 10px
        border-color black
    .upper
        margin-bottom  -15px
</style>
