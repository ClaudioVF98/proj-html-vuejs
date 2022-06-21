<template>
    <div>
        <div class="container">
            <div class="titles">

                <!-- Titoli -->
                <p class="mini-title">CORPORATE & WEDDINGS</p>
                <h1>Baking Special Moments</h1>
            </div>


            <div class="moments">
                <!-- Immaginie e info Plans -->
                <div class="plans">
                    <div class="centered-info">
                        <p>INTERNAL BAKERY</p>
                        <h1>Corporate Events</h1>
                        <button>Explore More</button>
                    </div>
                </div>

                <!-- Immagine e info Wedding -->
                <div class="wedding">
                    <div class="centered-info">
                        <p>PRIVATE DINING HALL</p>
                        <h1>Weddings & Parties</h1>
                        <button>Explore More</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>

export default {
    name: 'BakingOne',
    components: {
    }
}
</script>


<style scoped lang="scss">
.container {
    text-align: center;
    margin-bottom: 200px;

    // Titoli
    .titles {
        .mini-title {
            font-size: 12px;
            color: #b1a9b5;
            margin-bottom: 20px;
        }

        h1 {
            color: #55328b;
            font-size: 50px;
            margin-bottom: 20px;
        }
    }

    // Plans e Matrimonio
    .moments {
        display: flex;
        justify-content: space-evenly;
        height: 700px;

        .plans:hover .centered-info {
            display: flex;
        }

        .plans:hover {
            background-image: url("images/corporate-hover-bg.jpg");
            background-size: cover;
        }

        .plans {
            background-image: url("images/corporate-bg.jpg");
            background-size: cover;

            .centered-info * {
                margin-bottom: 10px;
            }

            .centered-info {
                flex-direction: column;
                justify-content: center;
                height: 100%;
                color: white;
                display: none;

                button:hover {
                    color: #55328b;
                    background-color: #f0edf5;
                }

                button {
                    width: 25%;
                    align-self: center;
                    padding: 3px;
                    color: white;
                    background-color: #55328b;
                    border: 0;
                    border-radius: 7px;
                    cursor: pointer;
                }
            }
        }


        .wedding:hover .centered-info {
            display: flex;
        }

        .wedding:hover {
            background-image: url("images/wedding-hover-bg.jpg");
            background-size: cover;
        }

        .wedding {
            background-image: url("images/wedding-bg.jpg");
            background-size: cover;

            .centered-info * {
                margin-bottom: 10px;
            }

            .centered-info {
                flex-direction: column;
                justify-content: center;
                height: 100%;
                color: white;
                display: none;

                button:hover {
                    color: #55328b;
                    background-color: #f0edf5;
                }

                button {
                    width: 25%;
                    align-self: center;
                    padding: 3px;
                    color: white;
                    background-color: #55328b;
                    border: 0;
                    border-radius: 7px;
                    cursor: pointer;
                }
            }
        }

        .plans,
        .wedding {
            width: 40%;

            img {
                width: 100%;
                object-fit: contain;
            }
        }
    }


}
</style>