<script>
    export default {
        name: 'everySingleCard',
        props: {
            titleInfo: Object
        }
    }
</script>


<template>
        <div class="card">
            <div class="img-container">
                <img :src="titleInfo.thumb" alt="">
            </div>
            <span>{{ titleInfo.series }}</span>
        </div>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;
.card{
    display: flex;
    flex-direction: column;
    width: calc(100%/6 - 20px);
    padding: 10px;
    margin: 10px;

    .img-container{
        
    }

    img{
        width: 100%;
        aspect-ratio: 1/1;
    }

    span{
        color: white;
        text-align: center;
        margin-top: 10px;
    }
}
</style>