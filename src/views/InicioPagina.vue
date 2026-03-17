<template>
    <div class="entorno">
        <div class="espacio">
            <div class="esp-izq">
                <div class="izq"></div>
            </div>
            <EspacioPublicar class="publicaciones"></EspacioPublicar>
            <div class="esp-der">
                <div class="der"></div>
            </div>
        </div>
    </div>
</template>

<script>
import EspacioPublicar from '@/components/EspacioPublicar.vue';


export default {
    name: 'InicioPagina',
    components: {
        EspacioPublicar,
    }
}
</script>

<style scoped>
* {
    margin-top: 5px;
    padding: 0;
    box-sizing: border-box;
}
.entorno {
    height: 100vh;
    display: flex;
    flex-direction: column;
    background-color: #ffffff;
}
.espacio {
    flex: 1;
    display: flex;
    overflow: hidden;
}
.esp-izq {
    height: 400px;
    width: 200px;
    background: #ffffff;
    border-right: 1px solid #000000;
    border-radius: 8px 0 0 8px;
}

.esp-der {
    height: 400px;
    width: 450px;
    background: #ffffff;
    padding: 1rem;
}
.der {
    height: 100%;
    width: 95%;
    background-color: #e0dfdf;
    border-radius: 8px;
}
</style>