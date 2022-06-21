<template>
    <div class="container">

        <!-- Informazioni e Pulsante Shop -->
        <div class="info-shop">
            <p>TRY OUR SEASONAL PRODUCTS</p>
            <h1>Order for pick-up or delivery to your home</h1>
            <button>Shop Now</button>
        </div>
    </div>
</template>


<script>


export default {
    name: 'ShopNow',
    components: {
    }
}
</script>


<style scoped lang="scss">
.container {
    width: 100%;
    height: 500px;
    background-image: url("images/call-to-action-bg.jpg");
    background-size: cover;
    margin-bottom: 50px;

    // Info
    .info-shop {
        width: 70%;
        height: 100%;
        margin: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;


        // Testo e Pulsante
        p {
            font-size: 12px;
            color: #b1a9b5;
            margin-bottom: 10px;
        }

        h1 {
            color: white;
            font-size: 50px;
            margin-bottom: 50px;
        }

        button {
            color: #55328b;
            background-color: white;
            border: 0;
            width: 7%;
            padding: 7px;
            border-radius: 7px;
            cursor: pointer;
        }
    }
}
</style>