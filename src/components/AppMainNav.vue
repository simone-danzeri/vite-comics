<script>
    export default {
        name: 'AppMainNav',
        data() {
            return {
                products: [
                    {
                        image: 'buy-comics-digital-comics.png',
                        text: 'DIGITAL COMICS',
                        active: false
                    },
                    {
                        image: 'buy-comics-merchandise.png',
                        text: 'DC MERCHANDISE',
                        active: false
                    },
                    {
                        image: 'buy-comics-subscriptions.png',
                        text: 'SUBSCRIPTION',
                        active: false
                    },
                    {
                        image: 'buy-comics-shop-locator.png',
                        text: 'COMIC SHOP LOCATOR',
                        active: false
                    },
                    {
                        image: 'buy-dc-power-visa.svg',
                        text: 'DC POWER VISA',
                        active: false
                    },
                ],
            }
        },
        methods: {
        getImageUrl(name) {
            return new URL(`../assets/img/${name}`, import.meta.url).href;
        }
    }
    }
</script>


<template>
    <section>
        <div class="container">
            <div class="products-container">
                <div class="products-content">
                    <div class="product" v-for="(product,index) in products">
                        <img :src="getImageUrl(product.image)">
                        <div class="product-name"><span>{{ product.text }}</span></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;

section{
    background-color: $brand-primary;
}
.products-container {
    height: 100px;
    padding: 25px;
}

.products-content {
    max-width: 100%;
    height: 100%;
    margin: auto;
    padding: 5px 20px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}


.product {
    width: calc(100%/5 - 10px);
    display: flex;
}

.product-name {
    display: flex;
    align-items: center;
    padding: 0 10px;
    color: white;
}
</style>