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
    height: 100vh;
    background: #fff;
}

.content {
    position: absolute;
    top: 30%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2em;
    width: 90%;
}

.title {
    font-size: 4em;
    margin: 0;
    font-weight: 800;
}

.title2 {
    font-size: 2.5em;
    font-weight: 200;
    margin: 0;
}
.title3 {
    font-size: 2.5em;
    font-weight: 800;
    margin: 0;
}

.button {
    font-family: 'Poppins';
    position: absolute;
    bottom: 20%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #FFA219;
    backdrop-filter: blur(2px);
    border-radius: 50px;
    border: none;
    font-size: 1.5em;
    padding: 10px 30px;
    color: #000;
    font-weight: 700;
}
</style>