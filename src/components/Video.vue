<template>
    <div class="container">
        <div class="content">
            <div class="video">
                <!-- Inserta la URL de tu video de YouTube aquí -->
                <iframe width="100%" height="315" src="https://www.youtube-nocookie.com/embed/fOW8Y09GVek"
                    title="YouTube video player" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                    allowfullscreen></iframe>
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
}

.content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: auto;
    padding: 3em;
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
    font-size: 2.2em;
    max-width: 550px;
}

.text-end {
    font-weight: 700;
    text-align: center;
    font-size: 2em;
    margin-top: 50px;
}

@media screen and (max-width: 850px) {
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
    }

}
</style>