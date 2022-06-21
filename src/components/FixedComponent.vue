<template>
    <div class="container">
        <div class="firstSquare">
            <font-awesome-icon icon="fa-regular fa-file" class="icon" />
            <p>Demos</p>
        </div>
        <div class="secondSquare">
            <p><span>$</span>39</p>
            <p>On Sale</p>
        </div>
    </div>
</template>


<script>

export default {
    name: 'FixedComponent',
    components: {
    }
}
</script>


<style scoped lang="scss">
.container {
    width: 80px;
    display: flex;
    flex-direction: column;
    position: fixed;
    right: 0;
    top: 200px;

    .firstSquare {
        width: 80px;
        height: 80px;
        border: 1px black solid;
        border-radius: 7px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 10px;
        background-color: white;
        cursor: pointer;

        .icon {
            font-size: 30px;
        }
    }

    .secondSquare {
        width: 80px;
        height: 80px;
        border: 1px black solid;
        border-radius: 7px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: white;
        padding: 10px;
        cursor: pointer;



        span {
            font-size: 10px;
            padding-bottom: 10px;
            position: relative;
            bottom: 7px;
        }

        p:first-of-type {
            color: green;
        }

        p {
            font-size: 16px;
        }
    }
}
</style>
