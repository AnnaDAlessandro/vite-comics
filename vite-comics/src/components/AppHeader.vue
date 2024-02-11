<script >
 export default{
    name:"AppHeader",
    data(){
        return{
            menuLinks:[
            {
                name:'CHARACTERS',
                current:false
            },
            {
                 name:'COMICS',
                 current:true
            },
            {
                name:'MOVIES',
                current:false
            },
            {
                name:'TV',
                current:false
            },
            {
                name:'GAMES',
                current:false
            },
            {
                name:'COLLECTIBLES',
                current:false
            },
            {
                name:'VIDEOS',
                current:false
            },
            {
                name:'FANS',
                current:false
            },
            {
                name:'NEWS',
                current:false
            },
            {
                name:'SHOP',
                current:false
            }
                  
            ]
        }
    }

 }
</script>

<template>
  <header>
    <div>
    <nav>
        <figure>
            <img src="../img/dc-logo.png" alt="" height="70">
        </figure>
        <ul>
            <li
            :class="element.current ? 'active-border-bottom' : ''"
            v-for="(element,index) in  menuLinks "
            :key="index">
                <a :class="element.current ? 'active' : ''" href="">{{element.name }}</a>
            </li>
        </ul>
    </nav>   
    </div>

  </header>
 
</template>

<style lang="scss" scoped>
 header{
    background-color: white;
    color: black;
    height: 100px;
    
    >div:first-child{
        margin: 0 auto;
        width: 80%;

    }

    nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    ul{
        display: flex;
        align-items: center;
        gap: 25px;
    }
    .active-border-bottom{
        border-bottom: 4px solid #0282f9;
    }
   .active{
    color: #0282f9;
   }
 }

</style>
