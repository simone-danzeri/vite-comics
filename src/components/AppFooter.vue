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
                    title: "DC",
                    links: ['Terms Of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    title: "SITES",
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
                {
                    title: "SHOP",
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
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
    <section class="bottom-footer">
        <div class="container">
            <div class="footer-bottom">
                <div class="btn-container">
                    <button>
                        <span>SIGN-UP NOW!</span>
                    </button>
                </div>
                <div class="social">
                    <h4>FOLLOW US</h4>
                    <div class="images">
                        <img src="../assets/img/footer-facebook.png" alt="fb logo">
                        <img src="../assets/img/footer-twitter.png" alt="twitter logo">
                        <img src="../assets/img/footer-youtube.png" alt="yt logo">
                        <img src="../assets/img/footer-pinterest.png" alt="pinterest logo">
                        <img src="../assets/img/footer-periscope.png" alt="perscope logo">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;

.top-footer{
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
}
.footer-top {
    margin: auto;
    padding: 40px 0;

    .links-container {
        width: 50%;
        display: flex;
        flex-wrap: wrap;

        &>div {
            padding: 0 35px;

            &:first-child{
                padding-left: 0px;
            }

            &:last-child{
                padding-left: 0px;
                margin-top: -94px;
            }
        }

        .links ul li {
            list-style-type: none;
            padding: 4px 0;
            
            a{
                text-decoration: none;
                color: $brand-secondary;
            }
        }

        .links h3 {
            color: white;
            padding-bottom: 20px;
        }
    }
}

.bottom-footer{
    background-color: #303030;
}
.footer-bottom{
    padding: 30px 0;
    display: flex;
    justify-content: space-between;
    .btn-container{
        button{
            border: 2px solid $brand-primary;
            background-color: #303030;
            padding: 14px 18px;
            cursor: pointer;

            span{
                color: white;
                font-size: 16px;
            }
        }
    }
    .social{
        display: flex;
        align-items: center;

        h4{
            color: $brand-primary;
            padding-right: 12px;
        }

        img{
            padding: 0 8px;
        }
    }
}
</style>