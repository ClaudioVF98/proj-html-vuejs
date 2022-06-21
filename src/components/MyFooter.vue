<template>
    <div class="container">

        <!-- Colonna di Sinistra -->
        <div class="left-div">

            <!-- Logo -->
            <div class="first-left-div">
                <img src="./images/avada-bakery-logo-retina-200x97.png" alt="">
            </div>

            <!-- Nav -->
            <div class="second-left-div">
                <p v-for="(item, i) in footerMenu" :key="i">{{ item }}</p>
                <p>
                    <font-awesome-icon icon="fa-solid fa-cart-shopping" /> <span>0</span>
                </p>
            </div>

            <!-- Copyright -->
            <div class="third-left-div">
                <p>© Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
            </div>
        </div>

        <!-- Colonna di Destra -->
        <div class="right-div">

            <!-- Subscribe -->
            <div class="first-right-div d-flex">
                <h1>Subscribe to Our Newsletter</h1>
            </div>

            <!-- Email e Subscribe Button -->
            <div class="second-right-div d-flex">
                <input type="text" placeholder="Enter Email Adress*">
                <button>Subscribe</button>
            </div>

            <!-- Brands -->
            <div class="third-right-div d-flex">
                <font-awesome-icon v-for="(brands, i) in footerMenuBrands" :icon="brands" :key="i" class="brands" />
            </div>

            <!-- Torna su -->
            <div class="fourth-right-div">
                <a href="#topPage">
                    <font-awesome-icon icon="fas fa-angle-up" class="iconUp" />
                </a>
            </div>
        </div>
    </div>
</template>


<script>

export default {
    name: 'MyFooter',
    components: {
    },
    data() {
        return {
            footerMenu: ['Shop', 'About', 'Gallery', 'Locations', 'Journal', 'Contact', 'Orders'],
            footerMenuBrands: ['fab fa-instagram', 'fab fa-twitter', 'fab fa-facebook-f', 'fab fa-pinterest-p']
        }
    }
}
</script>


<style scoped lang="scss">
.container {
    margin: 0 100px;
    display: flex;
    padding-bottom: 5px;

    .left-div {
        display: flex;
        flex-direction: column;
        width: 50%;

        .first-left-div {
            margin-bottom: 50px;

            img {
                cursor: pointer;
            }
        }

        .second-left-div {
            display: flex;
            justify-content: space-between;
            color: #55328b;
            margin-bottom: 100px;

            p {
                cursor: pointer;
            }

            span {
                background-color: #f0edf5;
                border-radius: 50%;
                padding: 5px;
            }
        }

        .third-left-div {
            p {
                font-size: 12px;
                color: #b1a9b5;
                margin-bottom: 10px;
            }
        }
    }

    .right-div {
        display: flex;
        flex-direction: column;
        width: 50%;

        .d-flex {
            display: flex;
            justify-content: flex-end;
            align-items: center;
        }

        .first-right-div {
            margin: 50px 0;

            h1 {
                color: #55328b;
            }
        }

        .second-right-div {
            margin-bottom: 80px;

            input {
                width: 35%;
                padding: 5px;
                margin-right: 10px;
                border-radius: 5px;
            }

            button {
                width: 20%;
                padding: 7px;
                color: white;
                background-color: #55328b;
                border: 0;
                border-radius: 5px;
                cursor: pointer;
            }

            button:hover {
                color: #55328b;
                background-color: #f0edf5;
            }
        }

        .third-right-div {
            color: #55328b;
            display: flex;
            justify-content: space-between;
            width: 20%;
            align-self: flex-end;
            margin: 0 20px 5px 0;

            .brands {
                cursor: pointer;
            }
        }

        .fourth-right-div {
            color: white;
            display: flex;
            justify-content: end;

            a {
                text-decoration: none;
                background-color: #474747;
                padding: 10px;
                border-radius: 7px;
                cursor: pointer;
                color: white;
            }
        }
    }
}
</style>