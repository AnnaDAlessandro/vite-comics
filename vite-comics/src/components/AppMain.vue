<script >
 export default{
 name:"AppMain",
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
        ]
    }
 }

 }
</script>

<template>
    <main>
      <div>
        <h2> -- > Content goes here &lt; --  </h2>
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
 div{
    padding: 50px 0;
    margin: 0 auto;
    width: 80%;
    h2{
        text-transform: capitalize;
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
                    img{
                        width: 60px;
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

