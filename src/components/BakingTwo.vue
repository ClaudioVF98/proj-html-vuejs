<template>
    <div class="container" id="gallery">

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
                    <img :src="items[activeSlide].photo" alt="">
                    <div>
                        <font-awesome-icon icon="fa-solid fa-angle-left" class="left arrow" @click="prevSlide()"/>
                    </div>
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>

                <div class="info">
                    <h2>{{ items[activeSlide].name }}</h2>
                    <p>{{ items[activeSlide].price }}</p>
                </div>
            </div>


            <div class="img-div pos-relative">
                <div class="image">
                    <img :src="items[secondActiveSlide].photo" alt="">
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>


                <div class="info">
                    <h2>{{ items[secondActiveSlide].name }}</h2>
                    <p>{{ items[secondActiveSlide].price }}</p>
                </div>
            </div>



            <div class="img-div pos-relative">
                <div class="image">
                    <img :src="items[thirdActiveSlide].photo" alt="">
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>
                <div class="info">
                    <h2>{{ items[thirdActiveSlide].name }}</h2>
                    <p>{{ items[thirdActiveSlide].price }}</p>
                </div>
            </div>



            <div class="img-div pos-relative">
                <div class="image">
                    <img :src="items[fourthActiveSlide].photo" alt="">
                    <div>
                        <font-awesome-icon icon="fa-solid fa-angle-right" class="right arrow" @click="nextSlide()" />
                    </div>
                    <div class="centered-info">
                        <p>SELECT OPTION / QUICK VIEW</p>
                    </div>
                </div>

                <div class="info">
                    <h2>{{ items[fourthActiveSlide].name }}</h2>
                    <p>{{ items[fourthActiveSlide].price }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'BakingTwo',
    components: {
    },
    data() {
        return {
            activeSlide: 0,
            secondActiveSlide: 1,
            thirdActiveSlide: 2,
            fourthActiveSlide: 3,
            items: [
                {
                    name: 'Choco Chip Cookies',
                    genre: 'Cookies, Pastries',
                    price: '$19.00 - $39.00',
                    photo: require('./images/choco-chip-cookies-400x510.jpg')
                },
                {
                    name: 'Strawberry Jam Cookies',
                    genre: 'Cookies, Pastries',
                    price: '$24.00 - $62.00',
                    photo: require('./images/strawberry-jam-cookies-400x510.jpg')
                },
                {
                    name: 'Strawberry Donut',
                    genre: 'Cookies, Pastries',
                    price: '$24.00 - $42.00',
                    photo: require('./images/strawberry-donut-400x510.jpg')
                },
                {
                    name: 'Perfect Macarons',
                    genre: 'Cookies, Pastries',
                    price: '$18.00 - 52.00',
                    photo: require('./images/perfect-macarons-400x510.jpg')
                },
                {
                    name: 'Blackberry Stuffed Bread',
                    genre: 'Cookies, Pastries',
                    price: '$25.00 - $63.00',
                    photo: require('./images/blackberry-stuffed-bread-400x510.jpg')
                },
                {
                    name: 'Cherry Cake',
                    genre: 'Cookies, Pastries',
                    price: '$30.00 - $91.00',
                    photo: require('./images/cherry-cake-400x510.jpg')
                },
                {
                    name: 'Cookies with Ice Cream',
                    genre: 'Cookies, Pastries',
                    price: '$23.00 - $37.00',
                    photo: require('./images/cookies-with-ice-cream-400x510.jpg')
                },
                {
                    name: 'Glazed Pancake with Lemon',
                    genre: 'Cookies, Pastries',
                    price: '$31.00 - $52.00',
                    photo: require('./images/glazed-pancake-with-lemon-400x510.jpg')
                },
                {
                    name: 'Home Bread',
                    genre: 'Cookies, Pastries',
                    price: '$11.00 - $27.00',
                    photo: require('./images/home-bread-400x510.jpg')
                },
                {
                    name: 'Premium Bread',
                    genre: 'Cookies, Pastries',
                    price: '$12.00 - $29.00',
                    photo: require('./images/premium-bread-400x510.jpg')
                },
                {
                    name: 'Small Cupcake',
                    genre: 'Cookies, Pastries',
                    price: '$17.00 - $28.00',
                    photo: require('./images/small-cupcake-400x510.jpg')
                }

            ]
        }
    },
    methods: {
        nextSlide() {
            this.activeSlide++;
            this.secondActiveSlide++;
            this.thirdActiveSlide++;
            this.fourthActiveSlide++;
            if (this.activeSlide + 1 > this.items.length - 1) {
                this.activeSlide = 0;
            } if (this.secondActiveSlide + 1 > this.items.length - 1) {
                this.secondActiveSlide = 0;
            } if (this.thirdActiveSlide + 1 > this.items.length - 1) {
                this.thirdActiveSlide = 0;
            } if (this.fourthActiveSlide + 1 > this.items.length - 1) {
                this.fourthActiveSlide = 0;
            }

        },
        prevSlide() {
            this.activeSlide--;
            this.secondActiveSlide--;
            this.thirdActiveSlide--;
            this.fourthActiveSlide--;
            if (this.activeSlide < 0) {
                this.activeSlide = this.items.length - 1;
            } if (this.secondActiveSlide < 0) {
                this.secondActiveSlide = this.items.length - 1;
            } if (this.thirdActiveSlide < 0) {
                this.thirdActiveSlide = this.items.length - 1;
            } if (this.fourthActiveSlide < 0) {
                this.fourthActiveSlide = this.items.length - 1;
            }
        }
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