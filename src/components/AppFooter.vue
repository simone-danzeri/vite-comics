<script>
    export default {
        name: 'AppFooter',
        data() {
        return {
            footerLinks: [
                {
                    title: "DC COMICS",
                    links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    title: "SHOP",
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    title: "DC",
                    links: ['Terms Of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    title: "SITES",
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                }
            ]
        }
    }
    }
</script>


<template>
    <section class="top-footer">
        <div class="container">
            <div class="footer-top">
                <div class="links-container">
                    <div class="links" v-for="eachObject in footerLinks">
                        <h3>{{ eachObject.title }}</h3>
                        <ul>
                            <li v-for="eachLink,index in eachObject.links">
                                <a href="#">{{ eachLink }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
.top-footer{
    background-image: url(../assets/img/footer-bg.jpg);
}
.footer-top {
    margin: auto;
    padding: 30px 0;

    .links-container {
        display: flex;
        flex-wrap: wrap;

        &>div {
            padding: 0 10px;
        }

        .links ul li {
            list-style-type: none;
            padding: 4px 0;
            
            a{
                text-decoration: none;
                color: #676b70;
            }
        }

        .links h3 {
            color: white;
            padding-bottom: 20px;
        }
    }
}
</style>