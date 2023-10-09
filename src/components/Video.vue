<template>
    <div class="container">
        <div class="content">
            <div class="video">
                <video controls width="100%" height="315" src="../assets/aguaViva.mp4"></video>
            </div>
            <div class="text">
                <p>Nuestras dificultades
                    son básicamente producto
                    de nosotr@s, surgen de
                    nosotr@s</p>
            </div>
        </div>
        <p class="text-end">¿estás dispuesto a hacer lo que sea necesario?</p>
    </div>
</template>

<script>
export default {
    name: 'Video'
}
</script>

<style scoped>
.container {
    width: 100%;
    height: 100%;
    padding-top: 100px;
    box-sizing: border-box;
}

.content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: auto;
    padding: 0 40px;
}

.video {
    width: 45%;
}

.text {
    width: 45%;
}

.text p {
    margin: 0;
    font-weight: 400;
    font-size: 30px;
    max-width: 550px;
}

.text-end {
    font-weight: 700;
    text-align: center;
    font-size: 2em;
    margin-top: 50px;
    padding-left: 20px;
    padding-right: 20px;
}

@media screen and (max-width: 1000px) {
    .content {
        flex-direction: column;
    }

    .video,
    .text {
        width: 100%;
    }

    .text p {
        max-width: 100%;
        margin-top: 10px;
        font-size: 1.5em;
    }

}

@media screen and (max-width: 400px) {

    .text p,
    .text-end {
        font-size: 1em;
    }
}

@media screen and (max-width: 576px) {

    .text p,
    .text-end {
        font-size: 1.4em !important;
    }

}

@media screen and (max-width: 768px) {

    .text p,
    .text-end {
        font-size: 1.5em;
    }
}

.video {
    position: relative;
}

.video::after {
    content: '';
    position: absolute;
    top: 50%;
    left: 53%;
    transform: translate(-50%, -50%);
    width: 100%;
    height: 80%;
    background: #FFA219;
    z-index: -1;
}
</style>