<template>
    <div >
       <v-layout row wrap fill-height>
           <v-flex md6>
               <v-layout column fill-height>
                   <v-flex>
                       <titlecontent :config="item"></titlecontent>
                   </v-flex>
                   <hr style="margin: 20px">
                   <v-flex>
                       <justtitle :config="item"></justtitle>
                   </v-flex>
               </v-layout>
           </v-flex>
           <v-flex md6>
               <v-layout column fill-height>
                   <v-flex md6>
                       <justimg :config="item"></justimg>
                   </v-flex>
                   <hr style="margin: 20px">
                   <v-flex md6>
                       <content1 :config="item"></content1>
                   </v-flex>
               </v-layout>
           </v-flex>
       </v-layout>
    </div>
</template>

<script>
import content1 from '~/components/contents/content1'
import justtitle from '~/components/contents/justtitle'
import titlecontent from "~/components/contents/titlecontent";
import justimg from "~/components/contents/justimg";
export default {
    data(){
        return{
            item:{
                img:'http://www.pcb.ub.edu/portal/image/journal/article?img_id=1412237&t=1517312061634',
                title:'This Module is an intro to the full article',
                dates:{words:'423 words',date:'Jan 2019'}, 
                content:'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not',
                minidate:'Tuesday, February 12'
            }
        }
    },
    components:{
        content1,
        justtitle,
        titlecontent,
        justimg
    }
}
</script>

<style>

</style>
