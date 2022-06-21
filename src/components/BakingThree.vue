<template>
    <div class="container">
        <!-- Primo Contenitore -->
        <div class="firstContainer">
            <div class="topDiv">
                <div class="top-left-div">
                    <h1 class="h1Title">Tell us what you have in mind</h1>
                </div>
                <div class="top-right-div">
                    <p class="pTitle">01</p>
                </div>
            </div>
            <div class="botDiv">
                <p class="mini-title">MANUAL INGREDIENTS SELECTION</p>
                <p class="mini-text">Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu
                    laoreet ex. Aliquam
                    erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem
                    erat, finibus in velit placerat, rutrum augue.</p>
            </div>
        </div>

        <!-- Secondo Contenitore -->
        <div class="secondContainer">
            <div class="mid-left-div">
                <div class="top-mid-left-div">
                    <h1>We Start Baking</h1>
                    <p>02</p>
                </div>

                <div class="bot-mid-left-div">
                    <p class="mini-title">SWEET & DELICIOUS</p>
                    <p class="mini-text">Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut
                        eu
                        laoreet ex. Aliquam
                        erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec
                        lorem
                        erat, finibus in velit placerat, rutrum augue.</p>
                </div>
            </div>

            <div class="mid-right-div">
                <p>DONT JUST TAKE OUR WORD FOR IT</p>
                <h1>"Finally found an alternative to the mass produced products. Something that incorporates real
                    organic ingredients, nutrient dense wellness while promoting sustainability and activity."</h1>
                <p>Rachel Cooper, Founder</p>
            </div>
        </div>

        <!-- Terzo Contenitore -->
        <div class="thirdContainer">
            <div class="top-div">
                <h1>Delivered to your home</h1>
                <p>03</p>
            </div>

            <div class="bot-div">
                <p>BAKED TO ORDER & GIFT WRAPPED</p>
                <p>Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu
                    laoreet ex. Aliquam
                    erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem
                    erat, finibus in velit placerat, rutrum augue.</p>
            </div>
        </div>
    </div>
</template>


<script>

export default {
    name: 'BakingThree',
    components: {
    }
}

</script>


<style scoped lang="scss">
.container {


    // Primo Contenitore
    .firstContainer::before {
        content: '';
        display: block;
        position: absolute;
        background-color: #000;
        opacity: 0.5;
        width: calc(100% - 200px);
        height: 700px;
        z-index: 1;
    }

    .firstContainer {
        background-image: url("images/bakery-process-1.jpg");

        margin: 0 100px;
        height: 700px;
        background-size: cover;
        margin-bottom: 20px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        .topDiv {
            display: flex;
            justify-content: space-between;
            padding: 100px;
            z-index: 2;

            .top-left-div {
                color: white;
                font-size: 25px;
            }

            .top-right-div {
                color: white;
                font-size: 70px;
            }
        }

        .botDiv {
            width: 30%;
            align-self: flex-end;
            margin: 0 50px 50px 0;
            z-index: 2;

            .mini-title {
                font-size: 18px;
                color: #b1a9b5;
                margin-bottom: 20px;
            }

            .mini-text {
                color: white;
                font-size: 20px;
            }
        }
    }


    // Secondo Contenitore
    .secondContainer {
        width: 100%;
        display: flex;
        margin-bottom: 20px;

        .mid-left-div::before {
            content: '';
            display: block;
            position: absolute;
            background-color: #000;
            opacity: 0.5;
            width: calc(50% - 140px);
            height: 700px;
            z-index: 1;
        }

        .mid-left-div {
            background-image: url("images/bakery-process-2.jpg");
            background-size: cover;
            width: 50%;
            margin: 0 50px 0 100px;
            height: 700px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            .top-mid-left-div {
                display: flex;
                justify-content: space-between;
                padding: 50px;
                z-index: 3;
                color: white;

                h1 {
                    font-size: 40px;
                }

                p {
                    font-size: 70px;
                }
            }

            .bot-mid-left-div {
                width: 50%;
                margin: 50px;
                z-index: 3;

                .mini-title {
                    font-size: 18px;
                    color: #b1a9b5;
                    margin-bottom: 20px;
                }

                .mini-text {
                    color: white;
                    font-size: 20px;
                }
            }
        }

        .mid-right-div {
            background-color: #f3eef4;
            width: 50%;
            height: 700px;
            margin-right: 100px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 100px;

            p {
                font-size: 12px;
                color: #b1a9b5;
                margin-bottom: 20px;
            }

            h1 {
                color: #55328b;
                font-size: 30px;
                margin-bottom: 20px;
            }
        }
    }


    // Terzo Contenitore
    .thirdContainer::before {
        content: "";
        display: block;
        position: absolute;
        background-color: #000;
        opacity: 0.5;
        width: calc(100% - 200px);
        height: 700px;
        z-index: 1;
    }

    .thirdContainer {
        background-image: url("images/bakery-process-3.jpg");
        margin: 0 100px;
        height: 700px;
        background-size: cover;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-bottom: 200px;

        .top-div {
            display: flex;
            justify-content: space-between;
            color: white;
            z-index: 3;
            padding: 50px;

            h1 {
                font-size: 40px;
            }

            p {
                font-size: 70px;
            }
        }

        .bot-div {
            width: 30%;
            padding: 50px;
            z-index: 3;

            p:first-of-type {
                font-size: 12px;
                color: #b1a9b5;
                margin-bottom: 20px;
            }

            p:last-of-type {
                color: white;
                font-size: 20px;
            }
        }
    }
}
</style>