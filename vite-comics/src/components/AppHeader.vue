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
    <nav>
        <figure>
            <img src="../img/dc-logo.png" alt="">
        </figure>
        <ul>
            <li
            v-for="(element,index) in  menuLinks "
            :key="index">
                <a href="">{{element.name }}</a>
            </li>
        </ul>
    </nav>
  </header>
 
</template>

<style lang="scss">
 header{
    background-color: white;
    color: black;
    padding: 15px;

    nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    ul{
        display: flex;
        align-items: center;
        gap: 25px;
        padding: 20px;

    }
  
 }

</style>
