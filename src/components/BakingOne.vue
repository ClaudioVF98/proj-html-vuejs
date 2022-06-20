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
                    <img src="./images/corporate-bg.jpg" alt="">
                </div>

                <!-- Immagine e info Wedding -->
                <div class="wedding">
                    <img src="./images/wedding-bg.jpg" alt="">
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
        .plans, .wedding {
            width: 40%;

            img {
                width: 100%;
                object-fit: contain;
            }
        }
    }


}
</style>