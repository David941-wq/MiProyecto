<template>
    <nav class="navegador">
      <div class="logo">
        <router-link to="/">
          <img src="@/assets/redit-png.png" alt="logo" class="logoP">
        </router-link>
      </div>
      <div>
          <input type="text" placeholder="Buscar..." class="busqueda">
      </div>
      <div class="opciones">
        <router-link v-for="ruta in rutas" :key="ruta.path" :to="ruta.path" exact-active-class="active">{{ ruta.nombre }}</router-link>
      </div>
    </nav>
</template>

<script>
export default {
  data() {
    return {
      rutas: [
        {nombre: 'InicioPagina', path: '/inicioPagina'},
        {nombre: '', path: ''},
      ]
    }
  }
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
/*Desde aqui empieza la decoracion normal de la barra en general*/
.navegador {
  height: 85px;
  width: 100%;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  background-color: #bb8686;
  align-items: center;
  position: fixed;
}
.logo img {
  height: 50px;
  width: 60px;
}
/*Aqui es el estilo que tendran las opciones que nos redirigen*/
.opciones {
  height: 100%;
  display: flex;
  gap: 20px;
  justify-content: center;
  align-items: center;
}
.opciones a {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px 15px;
  border-radius: 10px;
  color: white;
  text-decoration: none;
  transition: 0.25s ease;
}
.opciones a:hover {
  text-decoration: none;
  color: #403e3d;
  transition: color 0.3s;
}
/*Aqui empieza y ala barra de busqueda y su estilo*/
.busqueda {
  height: 30px;
  width: 600px;
  border-radius: 15px;
  border: none;
  padding: 0.5rem;
}
</style>