<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                links: [
                    {
                        text: 'CHARACTERS',
                        active: false
                    },
                    {
                        text: ' COMICS',
                        active: false
                    },
                    {
                        text: 'MOVIE',
                        active: false
                    },
                    {
                        text: 'TV',
                        active: false
                    },
                    {
                        text: 'GAMES',
                        active: false
                    },
                    {
                        text: 'COLLECTIBLES',
                        active: false
                    },
                    {
                        text: 'VIDEOS',
                        active: false
                    },
                    {
                        text: 'FANS',
                        active: false
                    },
                    {
                        text: 'NEWS',
                        active: false
                    },
                    {
                        text: 'SHOP',
                        active: false
                    },
                ],
            }
        }
    }
</script>


<template>
    <header>
        <div class="container">
            <div class="header-container">
                <div class="logo">
                    <div class="img-container">
                        <img src="../assets/img/dc-logo.png" alt="">
                    </div>
                </div>
                <nav>
                    <ul>
                        <li v-for="eachLink in links">
                            <a :class="{'active': eachLink.active}" href="#">{{ eachLink.text }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>


<style scoped lang="scss">
header{
    
    img{
        width: 90px;
        height: 90px;
    }
    .header-container{
        padding: 20px 0;
        display: flex;
        justify-content: space-between;
        align-content: center;
    }
    nav{
        display: flex;
        align-items: center;

        ul{
            display: flex;
            li{
                list-style: none;
                padding: 0 15px;
                
                &:last-child{
                    padding-right: 0;
                }
                .active{
                    color: blue;
                }
                
                a{
                    font-size: 15px;
                    text-decoration: none;
                    color: #676b70;
                }
            }
        }
    }
}

</style>