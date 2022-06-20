<template>
    <div class="container">
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



<style lang="scss">
.container {
    height: 1200px;
    background-image: url("images/hero-header-bakery.jpg");
    background-size: cover;

    .header {
        align-items: center;
        display: flex;
        flex-direction: row;
        height: 120px;

        .left-header {
            width: 50%;

            img {
                padding: 5px;
            }
        }

        .right-header {
            width: 50%;
            display: flex;
            justify-content: space-evenly;

            p {
                text-decoration: none;
                color: #55328b;
                margin: 0 10px;

            }
        }

    }

    .mid-div-container * {
        margin: 10px 0;
    }

    .mid-div-container {
        width: 25%;
        display: flex;
        flex-direction: column;
        height: calc(100% - 120px);
        justify-content: center;
        margin: 0 50px;

        .mini-title {
            font-size: 10px;
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
        }
    }
}
</style>
