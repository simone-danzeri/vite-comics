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
                        <li v-for="eachLink,index in links">
                            <a :class="{'active': eachLink.active}" href="#" @click="eachLink.active = !eachLink.active" >{{ eachLink.text }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;

header{
    
    .logo{
        display: flex;
        align-items: center;
    }

    img{
        width: 90px;
        height: 90px;
    }
    .header-container{
        /* padding: 20px 0; */
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
                padding: 0px 15px;
                height: 120px;
                display: flex;
                align-items: center;
                
                &:last-child{
                    padding-right: 0;
                }
                .active{
                    color: $brand-primary;
                    border-bottom: 2px solid $brand-primary;
                }
                
                a{
                    font-size: 15px;
                    text-decoration: none;
                    color: $brand-secondary;
                }
            }
        }
    }
}

</style>