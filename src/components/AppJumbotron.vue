<script>
    export default {
        
    }
</script>
<template>
    <section>
        <div>
            <h3>CURRENT SERIES</h3>
        </div>
    </section>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;
section{
    background-image: url(../assets/img/jumbotron.jpg);
    height: 450px;
    position: relative;

    div{
        background-color: $brand-primary;
        padding: 10px 20px;
        position: absolute;
        top: 95%;
        left: 15%;
        h3{
            color: white;
        }
    }
}
</style>