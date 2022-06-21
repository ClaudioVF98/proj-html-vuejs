<template>
    <div class="container" id="shop">
        <!-- Contenitore a sinistra con Pulsante Shopping -->
        <div class="left-div">
            <p class="mini-title">OUR PRODUCTS</p>
            <h1>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural,
                all organic ingredients.</h1>
            <button>Start Shopping</button>
        </div>

        <!-- Contenitore a destra con Arrow di scorrimento -->
        <div class="right-div">
            <div class="image-div">
                <img :src='items[activeSlide].photo' alt="">
                <div>
                    <font-awesome-icon icon="fa-solid fa-angle-left" class="left arrow" @click="prevSlide()" />
                </div>
                <div class="centered-info">
                    <h2>{{ items[activeSlide].name }}</h2>
                    <p>{{ items[activeSlide].genre }}</p>
                    <h3>{{ items[activeSlide].price }}</h3>
                </div>
            </div>



            <div class="image-div">
                <img :src="items[secondActiveSlide].photo" alt="">
                <div>
                    <font-awesome-icon icon="fa-solid fa-angle-right" class="right arrow" @click="nextSlide()" />
                </div>
                <div class="centered-info">
                    <h2>{{ items[secondActiveSlide].name }}</h2>
                    <p>{{ items[secondActiveSlide].genre }}</p>
                    <h3>{{ items[secondActiveSlide].price }}</h3>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'MainBot',
    components: {
    },
    data() {
        return {
            activeSlide: 0,
            secondActiveSlide: 1,
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
            if (this.activeSlide + 1 > this.items.length - 1) {
                this.activeSlide = 0;
            }
            if (this.secondActiveSlide + 1 > this.items.length - 1) {
                this.secondActiveSlide = 0;
            }

        },
        prevSlide() {
            this.activeSlide--;
            this.secondActiveSlide--;
            if (this.activeSlide < 0) {
                this.activeSlide = this.items.length - 1;
            }
            if (this.secondActiveSlide < 0) {
                this.secondActiveSlide = this.items.length - 1;
            }
        }
    }
}

</script>

<style scoped lang="scss">
.container {
    display: flex;
    margin: 0px 50px 100px 50px;

    // Stili contenitore sinistra
    .left-div * {
        margin-bottom: 20px;
    }


    .left-div {
        width: 40%;
        margin: 0 100px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        .mini-title {
            font-size: 12px;
            color: #b1a9b5;
        }

        h1 {
            color: #55328b;
            font-size: 50px;
        }

        button {
            width: 20%;
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

    // Stili contenitori destra

    .right-div {
        width: 60%;
        display: flex;
        justify-content: center;
    }

    // Freccette e immagini

    .image-div:hover .centered-info {
        display: flex;
        flex-direction: column;
        justify-content: center;

    }

    .image-div {
        position: relative;
        margin: 5px;

        .arrow {
            position: absolute;
            font-size: 20px;
            background-color: rgba(85, 50, 139, 0.5);
            padding: 10px 5px;
            cursor: pointer;
            margin: 0;
            z-index: 4;
        }

        .centered-info * {
            margin-bottom: 15px;
        }

        .centered-info {
            content: '';
            background-color: #000;
            opacity: 0.5;
            width: 100%;
            height: calc(100%);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            display: none;
            text-align: center;
            z-index: 3;
            color: white;
        }

        .left {
            top: 50%;
        }

        .right {
            top: 50%;
            right: 0%;
        }
    }
}
</style>