<template>
    <div>
        <v-layout>
            <v-flex>
                <p>{{TodayDate}} &nbsp| &nbsp </p>
            </v-flex>
            <v-flex>
                <p>
                    <v-icon>cloud</v-icon>
                    {{weather}}
                </p>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
export default {
    data(){
        return{
            TodayDate:'',
            weather:''
        }
    },
    mounted() {
        var meses = new Array ("Enero","Febrero","Marzo","Abril","Mayo","Junio","Julio","Agosto","Septiembre","Octubre","Noviembre","Diciembre");
        var diasSemana = new Array("Domingo","Lunes","Martes","Miércoles","Jueves","Viernes","Sábado");
        var f=new Date();
        this.TodayDate = diasSemana[f.getDay()] + ", " + f.getDate() + " de " + meses[f.getMonth()] + " de " + f.getFullYear();
        debugger
        this.$axios.get('api.openweathermap.org/data/2.5/weather?id=2172797').then((res)=>{
            debugger 
            this.weather = res
        })
    },
}
</script>

<style>

</style>
