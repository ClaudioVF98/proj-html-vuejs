<template>
    <div class="container">
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
                <img src="./images/choco-chip-cookies-400x510.jpg" alt="">
                <div>
                    <font-awesome-icon icon="fa-solid fa-angle-left" class="left arrow" />
                </div>
                <div class="centered-info">
                    <h2>Choco Chip Cookies</h2>
                    <p>Cookies, Pastries</p>
                    <h3>$19.00 - $39.00</h3>
                </div>
            </div>
            <div class="image-div">
                <img src="./images/strawberry-jam-cookies-400x510.jpg" alt="">
                <div>
                    <font-awesome-icon icon="fa-solid fa-angle-right" class="right arrow" />
                </div>
                <div class="centered-info">
                    <h2>Strawberry Jam Cookies</h2>
                    <p>Cookies, Pastries</p>
                    <h3>$24.00 - $62.00</h3>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'MainBot',
    components: {
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