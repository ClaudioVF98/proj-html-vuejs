<template>
    <div class="container-main-top">

        <!-- Header con Menu Nav -->
        <div class="header">
            <div class="left-header">
                <img src="./images/avada-bakery-logo-retina-200x97.png" alt="">
            </div>

            <div class="right-header">
                <p href="" v-for="(item, i) in menu" :key="i">
                    {{ item }}
                </p>
                <p href="">
                    <font-awesome-icon icon="fa-solid fa-cart-shopping" />
                </p>
            </div>
        </div>

        <!-- Div centrale con Bottone -->
        <div class="mid-div-container">
            <p class="mini-title">FRESH & TASTY BAKERY EVERY DAY</p>
            <h1>The Perfect Fresh Bread</h1>
            <p class="sub-text">Cras consequat lectus vestibulum tortor pulinar, quis euismod nist varius. Aliquam erat
                volutpat. Nullam quis sagittis nibh ac nulla id orci tempor.</p>
            <button>Explore our products</button>
        </div>
    </div>
</template>

<script>


export default {
    name: 'MainTop',
    components: {
    },
    data() {
        return {
            menu: ['HOME', 'SHOP', 'ABOUT', 'GALLERY', 'LOCATIONS', 'JOURNAL', 'CONTACT', 'MY ACCOUNT']
        }
    }
}
</script>



<style scoped lang="scss">

// Background e altezza
.container-main-top {
    height: 1200px;
    background-image: url("images/hero-header-bakery.jpg");
    background-size: cover;
    margin-bottom: 100px;

    .header {
        align-items: center;
        display: flex;
        flex-direction: row;
        height: 120px;

        // Logo
        .left-header {
            width: 50%;

            img {
                padding: 5px;
            }
        }

        // Nav Menu
        .right-header {
            width: 50%;
            display: flex;
            justify-content: space-evenly;

            p {
                text-decoration: none;
                color: #55328b;
                margin: 0 10px;
                cursor: pointer;

            }
        }

    }


    // Div Centrale con info sul prodotto
    .mid-div-container * {
        margin: 10px 0;
    }

    .mid-div-container {
        width: 25%;
        display: flex;
        flex-direction: column;
        height: calc(100% - 120px);
        justify-content: center;
        margin: 0 100px;

        .mini-title {
            font-size: 12px;
            color: #b1a9b5;
        }

        h1 {
            color: #55328b;
            font-size: 50px;
        }

        .sub-text {
            color: #888390;
            font-size: 20px;
        }
        
        button {
            width: 30%;
            padding: 8px;
            border: 0;
            background-color: white;
            color: #55328b;
            cursor: pointer;
            border-radius: 7px;
        }
    }
}
</style>
