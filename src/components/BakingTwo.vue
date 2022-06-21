<template>
    <div class="container">

        <!-- Info Prodotto + Shop Button -->
        <div class="left-div">
            <h1>Find a freshly baked product perfect for you</h1>
            <p class="mini-title">Integer a nibh ex porttitor retrum et ut velit. Etiam ac felis at leo feugiat
                placerat. Sed ac nulla id orci tempor convallis sed.</p>
            <button>Shop All Products</button>
        </div>

        <!-- Prodotti con prezzi -->
        <div class="right-div">
            <div class="img-div pos-relative">
                <div class="image">
                    <img src="./images/choco-chip-cookies-400x510.jpg" alt="">
                    <div>
                        <font-awesome-icon icon="fa-solid fa-angle-left" class="left arrow" />
                    </div>
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>

                <div class="info">
                    <h2>Choco Chip Cookies</h2>
                    <p>$19.00 - $39.00</p>
                </div>
            </div>


            <div class="img-div pos-relative">
                <div class="image">
                    <img src="./images/strawberry-jam-cookies-400x510.jpg" alt="">
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>


                <div class="info">
                    <h2>Strawberry Jam Cookies</h2>
                    <p>$24.00 - $62.00</p>
                </div>
            </div>



            <div class="img-div pos-relative">
                <div class="image">
                    <img src="./images/strawberry-donut-400x510.jpg" alt="">
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>
                <div class="info">
                    <h2>Strawberry Donut</h2>
                    <p>$24.00 - $42.00</p>
                </div>
            </div>



            <div class="img-div pos-relative">
                <div class="image">
                    <img src="./images/perfect-macarons-400x510.jpg" alt="">
                    <div>
                        <font-awesome-icon icon="fa-solid fa-angle-right" class="right arrow" />
                    </div>
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>

                <div class="info">
                    <h2>Perfect Macarons</h2>
                    <p>$18.00 - $52.00</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'BakingTwo',
    components: {
    }
}

</script>

<style scoped lang="scss">
.container {
    display: flex;
    width: 100%;
    margin-bottom: 100px;

    // Shop + Info e bottone
    .left-div {
        text-align: center;
        width: 25%;
        margin: 0 100px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        h1 {
            color: #55328b;
            font-size: 50px;
            margin-bottom: 20px;
        }

        .mini-title {
            font-size: 18px;
            color: #b1a9b5;
            margin-bottom: 20px;
        }

        button {
            width: 25%;
            border: 0px;
            background-color: #55328b;
            color: white;
            border-radius: 7px;
            padding: 8px;
            cursor: pointer;
        }

        button:hover {
            background-color: #f0edf5;
            color: #55328b;
        }
    }

    // Prodotti e prezzi

    .right-div {
        display: flex;
        width: 60%;


        .img-div {
            width: calc(100% / 4);
            margin-right: 10px;
            display: flex;
            flex-direction: column;

            .image:hover .centered-info {
                display: flex;
                flex-direction: column;
                justify-content: center;
            }

            // position: relative;
            .image {

                .centered-info {
                    content: '';
                    background-color: #000;
                    opacity: 0.5;
                    width: 100%;
                    height: calc(100% - 60px);
                    position: absolute;
                    top: 0%;
                    left: 50%;
                    transform: translate(-50%, -0%);
                    display: none;
                    text-align: center;
                    z-index: 3;
                    color: white;
                }
            }
        }

        img {
            width: 100%;
        }

        h2 {
            text-align: center;
            margin-bottom: 10px;
            color: #55328b;
        }

        p {
            text-align: center;
            color: #825f9c;
        }

        .pos-relative {
            position: relative;
        }

        .arrow {
            position: absolute;
            font-size: 20px;
            background-color: rgba(85, 50, 139, 0.5);
            padding: 10px 5px;
            cursor: pointer;
            margin: 0;
            z-index: 4;
        }

        .left {
            top: 40%;
        }

        .right {
            top: 40%;
            right: 0%;
        }
    }
}
</style>