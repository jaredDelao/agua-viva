<template>
    <div class="container">
        <div class="content">
            <h1 class="title">¿Te quieres recuperar?</h1>
            <p class="title2">Sin ayuda resulta demasiado,</p>
            <p class="title3">AV tiene la clave</p>
        </div>
        <button type="button" class="button">Únete a nuestra comunidad</button>
    </div>
</template>

<script>
export default {
    name: 'Principal',
    setup() {

    }
}
</script>

<style scoped>
.container {
    background: #fff;
    position: relative;
    height: 100%;
    text-align: center;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 100px;
    padding-bottom: 50px;
}

.content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
}

.title {
    font-size: 4em;
    margin: 0;
    font-weight: 800;
    text-align: center;
    margin-bottom: 15px;
    line-height: 1em;
}

.title2 {
    font-size: 2.5em;
    font-weight: 200;
    margin: 0;
    margin-bottom: 15px;
    text-align: center;
}
.title3 {
    font-size: 2.5em;
    font-weight: 800;
    margin: 0;
    text-align: center;
}

.button {
    font-family: 'Poppins';
    background: #FFA219;
    backdrop-filter: blur(2px);
    border-radius: 50px;
    border: none;
    font-size: 1.5em;
    padding: 10px 30px;
    color: #000;
    font-weight: 700;
    max-width: 500px;
    margin-top: 150px;
}

@media screen and (max-width: 400px) {
    .title {
        font-size: 2em !important;
    }
    .title3 {
        font-size: 1em;
    }
}

@media screen and (max-width: 576px) {
    .title {
        font-size: 3em !important;
    }
    .title2,
    .title3 {
        font-size: 1.4em !important;
    }
    .button {
        font-size: 0.9em;
        width: 100%;
    }
}

@media screen and (max-width: 768px) {
    .title {
        font-size: 3em;
    }
    .title2,
    .title3 {
        font-size: 1.5em;
    }

    .button {
        font-size: 1em;
    }
}
</style>