<template>
    <div class="container">

        <!-- Titoli -->
        <p>Loactions</p>
        <h1>Visit our Bakeries</h1>

        <!-- Informazioni, orari e immagini dei negozi -->
        <div class="images-time">

            <!-- New York -->
            <div class="left-div">
                <div class="top-left-div"></div>
                <div class="bot-left-div">
                    <div class="top">
                        <h1>New York</h1>
                    </div>
                    <div class="bot">
                        <div>
                            <p>CALL US</p>
                            <p>1.800.458.556</p>
                        </div>
                        <div>
                            <p>OPEN ALL WEEK</p>
                            <p>9:00 AM - 6:00 PM</p>
                        </div>
                        <div>
                            <button>View Map</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Londra -->
            <div class="right-div">
                <div class="top-right-div"></div>
                <div class="bot-right-div">
                    <div class="top">
                        <h1>London</h1>
                    </div>
                    <div class="bot">
                        <div>
                            <p>CALL US</p>
                            <p>1.800.458.556</p>
                        </div>
                        <div>
                            <p>OPEN ALL WEEK</p>
                            <p>9:00 AM - 6:00 PM</p>
                        </div>
                        <div>
                            <button>View Map</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>


export default {
    name: 'LocationAndTimeTable',
    components: {
    }
}
</script>


<style scoped lang="scss">
.container {
    margin: 0 100px 200px 100px;

    // Titoli
    p,
    h1 {
        text-align: center;
        margin-bottom: 10px;
    }

    p {
        font-size: 12px;
        color: #b1a9b5;
        margin-bottom: 20px;
    }

    h1 {
        color: #55328b;
        font-size: 40px;
    }


    // Negozi
    .images-time {
        display: flex;
        width: 100%;


        // New York
        .left-div {
            width: 50%;

            .top-left-div {
                background-image: url("images/new-york-bk-1200x794.jpg");
                width: 100%;
                height: 700px;
                background-size: cover;
            }

            .bot-left-div {
                background-color: #f1f9fb;
                width: 100%;
                height: 200px;
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;

                .bot {
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;

                    button {
                        background-color: white;
                        border: 0;
                        color: #603f92;
                        padding: 7px;
                        border-radius: 7px;
                        cursor: pointer;
                    }
                }
            }
        }
        

        // Londra
        .right-div {
            width: 50%;

            .top-right-div {
                background-image: url("images/london-bk-1200x794.jpg");
                width: 100%;
                height: 700px;
                background-size: cover;
            }

            .bot-right-div {
                background-color: #faf3e3;
                width: 100%;
                height: 200px;
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;

                .bot {
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;

                    button {
                        background-color: white;
                        border: 0;
                        color: #603f92;
                        padding: 7px;
                        border-radius: 7px;
                        cursor: pointer;
                    }
                }
            }
        }
    }
}
</style>