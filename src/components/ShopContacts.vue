<template>
    <div class="container">

        <!-- Due immagini più tasto contatto Instagram -->
        <div class="top">
            <div class="top-div m-right">
                <img src="./images/social-1.jpg" alt="">
            </div>
            <div class="longer-top-div m-right">
                <p>MADE FOR SHARING</p>
                <h1>Let's stay in touch</h1>
                <button>
                    <font-awesome-icon icon="fab fa-instagram" /> Follow us
                </button>
            </div>
            <div class="top-div">
                <img src="./images/social-2.jpg" alt="">
            </div>
        </div>

        <!-- Quattro immagini -->
        <div class="bot">
            <div class="bot-div m-right">
                <img src="./images/social-3.jpg" alt="">
            </div>
            <div class="bot-div m-right">
                <img src="./images/social-4.jpg" alt="">
            </div>
            <div class="bot-div m-right">
                <img src="./images/social-5.jpg" alt="">
            </div>
            <div class="bot-div">
                <img src="./images/social-6.jpg" alt="">
            </div>
        </div>
    </div>
</template>


<script>

export default {
    name: 'ShopContacts',
    components: {
    }
}
</script>


<style scoped lang="scss">
.container {
    margin: 0 100px 100px 100px;
    display: flex;
    flex-direction: column;

    // Immagini e margine
    .top {
        display: flex;
        margin-bottom: 20px;

        .m-right {
            margin-right: 20px;
        }

        .top-div {
            width: 25%;
            height: 400px;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        // IG
        .longer-top-div {
            width: 50%;
            height: 400px;
            background-color: #f7f0f2;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;

            p {
                font-size: 12px;
                color: #b1a9b5;
                margin-bottom: 20px;
            }

            h1 {
                color: #55328b;
                font-size: 40px;
                margin-bottom: 20px;
            }

            button {
                align-self: center;
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
    }


    // Immagini e margine
    .bot {
        display: flex;

        .m-right {
            margin-right: 20px;
        }

        .bot-div {
            width: 25%;
            height: 400px;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;

            }
        }
    }
}
</style>