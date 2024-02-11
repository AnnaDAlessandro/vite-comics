<script >
import FumettoCards from './FumettoCards.vue';


 export default{
 name:"AppMain",
 components:{
  FumettoCards
 },
 data(){
    return{
menuImage:[
            { 
                name:"DIGITAL COMICS",
                image:"buy-comics-digital-comics.png"
            },
            { 
                name:"DC MERCHANDISE",
                image:"buy-comics-merchandise.png"
            },
            { 
                name:"SUBSCRIPTIONS",
                image:"buy-comics-subscriptions.png"
            },
             { 
                name:"COMICS SHOP LOCATOR",
                image:"buy-comics-shop-locator.png"

            },
            { 
                name:"DC POWER VISA",
                image:"buy-dc-power-visa.svg"
            }
        ],
        arrayFumetti:[
        
        {
            "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book",
        },
        {
            "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book",
        },
        {
            "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel",
        },
        {
            "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book",
        },
        {
            "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book",
        },
        {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel",
        },
      ]
      
    }
 }

 }
</script>

<template>
    <main>
        <div class="jumbatron">

        </div>
      <div>
        <h2> Current Series  </h2>
        <div class="row">
         <FumettoCards
         v-for="(element,index) in arrayFumetti"
         :key="index"
         :propsThumb="element.thumb"
         :propsSeries="element.series">

         </FumettoCards>
        </div>
      </div> 
      <div class="bg-blue">
        <div>
            <ul>
                <li
                v-for="(element,index) in menuImage"
                :key="index"> 
                <figure>
                    <img :src="`./src/img/${element.image} `" alt="">
                </figure>
                <span>{{ element.name }}</span></li>
            </ul>
        </div>

      </div> 
      
    </main>
  
 
</template>

<style lang="scss" scoped>
main{
  .jumbatron{
    background-image: url(../img/jumbotron.jpg);
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 350px;
  }
 >div:nth-child(2){
    padding: 50px 0;
    margin: 0 auto;
    width: 80%;
    position: relative;
    h2{
        position: absolute;
        text-transform: uppercase;
        font-size: 18px;
        background-color: #0282f9;
        padding: 10px;
        top: -20px;
    }
    .row{
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        margin-top: 20px;
    }
}  
.bg-blue{
    background-color:#0282f9;
    width: 100%;
    color: white;
    padding: 30px 0;
    >div{
        margin: 0 auto;
        width: 80%;
        ul{
            display: flex;
            justify-content: space-between;
            align-items: center;
            li{
                display: flex;
                align-items: center;
                gap: 20px;
                figure{
                    display: flex;
                    align-items: center;
                    img{
                        height: 60px;
                    }
                }
                span{
                    color: white;
                }
            }

        }
        }
    }
} 



</style>

