<template>
    <div class="wrapper">
        <div class="title">
            <h2>Método de recuperación</h2>
        </div>
        <div class="grid-container">
            <div class="grid-item">
                <img src="../assets/steps/1.svg" alt="1">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/2.svg" alt="2">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/3.svg" alt="3">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/4.svg" alt="4">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/5.svg" alt="5">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/6.svg" alt="6">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/7.svg" alt="7">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/8.svg" alt="8">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/9.svg" alt="9">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/10.svg" alt="10">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/11.svg" alt="1">
            </div>
            <div class="grid-item">
                <img src="../assets/steps/12.svg" alt="12">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Steps'
}
</script>

<style scoped>

.wrapper {
    padding: 100px 20px;
}
.title h2 {
    font-weight: 700;
    font-size: 4em;
    text-align: center;
    margin-bottom: 30px;
    line-height: 1em;
    margin-top: 0;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 10px;
    margin: 0 auto;
}

.grid-item {
    text-align: center;
}

.grid-item img {
    width: 100%;
    max-width: 200px;
    min-width: 50px;
}

@media (max-width: 768px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }

    .title h2 {
        font-size: 2.5em;
    }
}

@media (max-width: 480px) {
    .grid-container {
        grid-gap: 0;
        padding: 0;
    }
}
</style>