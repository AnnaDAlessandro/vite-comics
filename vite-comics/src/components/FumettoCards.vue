    <script >
    
     export default{
        name:"FumettoCards",
        props:{
            propsThumb:String,
            propsSeries:String

        },
        data(){
            return{
               
   
            }
        }
       
     }
    </script>
    
    <template>
        <div class="col-2">
         <figure>
            <img :src="propsThumb" alt="">
         </figure>
         <h4>
            {{propsSeries}}
         </h4>
        </div>
    
     
    </template>
    
    <style lang="scss" scoped>
    .col-2{
        flex-basis: calc(100% / 6 - 20px);
        figure{
            img{
                width: 100%;
                display: block;
            }
    
        }
    }
    
    </style>