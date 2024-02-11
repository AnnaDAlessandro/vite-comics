<script >
export default{
name:"AppFooter",
data(){
    return{
        menuLinkFooterDcComincs:[
            {
                name:'Characters',
                link:'#'
            },
            {
                name:'Comics',
                link:'#'
            },
            {
                name:'Movies',
                link:'#'
            },
            {
                name:'TV',
                link:'#'
            },
            {
                name:'Games',
                link:'#'
            },
            {
                name:'Videos',
                link:'#'
            },
            {
                name:'News',
                link:'#'
            }
        ],
        menuLinkFooterShop:[
            {
                name:'Shop DC',
                link:'#'
            },
            {
                name:'Shop DC Collectibles',
                link:'#'
            }
    ],
         menuLinkFooterDc:[
            {
                name:'Terms of use',
                link:'#'
            },
            {
                name:'Privacy policy (New)',
                link:'#'
            },
            {
                name:'Ad Choices',
                link:'#'
            },
            {
                name:'Advertising ',
                link:'#'
            },
            {
                name:'Jobs',
                link:'#'
            },
            {
                name:'Subscriptions',
                link:'#'
            },
            {
                name:'Talent Workshops',
                link:'#'
            },
            {
                name:'CPSC Certificates',
                link:'#'
            },
            {
                name: 'Ratings',
                link:'#'
            },
            {
                name:'Shop help',
                link:'#'
            },
            {
                name:'Contact Us',
                link:'#'
            }
           
         ],
         menuLinkFooterSites:[
            {
                name:'DC',
                link:'#'
            },
            {
                name:'MAD Magazine',
                link:'#'
            },
            {
                name:'DC Kids',
                link:'#'
            },
            {
                name:'DC Universe',
                link:'#'
            },
            {
                name:'DC Power Visa',
                link:'#'
            }

         ]


    }
}

}
</script>

<template>
    <footer>
        <div>
            <nav>
                <div>
                    <h5>DC COMICS</h5>
                    <ul>
                        <li
                        v-for="(element,index) in menuLinkFooterDcComincs"
                        :key="index">
                            <a href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                    
                    <h5>SHOP</h5>
                    <ul>
                        <li
                        v-for="(element,index) in menuLinkFooterShop"
                        :key="index">
                            <a href="element.link"> {{element.name }}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <H5>DC</H5>
                    <ul>
                        <li
                        v-for="(element,index) in menuLinkFooterDc"
                        :key="index">
                            <a href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <H5>SITES</H5>
                    <ul>
                        <li
                        v-for="(element,index) in menuLinkFooterSites"
                        :key="index">
                            <a href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>

    </footer>
  
 
</template>

<style lang="scss" scoped>
footer{
    background-image: url('../img/footer-bg.jpg');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    padding: 30px 0;
    >div:first-child{
        margin: 0 auto;
        width: 80%;
        nav{
            display: flex;
            gap: 50px;
            h5{
                margin-top: 10px;
                margin-bottom: 10px;

            }
            ul{
                li{
                    a{
                        color: #6d6d6d;
                    }
                }

            }
             
        }
    }
}

</style>
