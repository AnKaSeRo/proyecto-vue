<script>
  import Pub from './components/Pub.vue'
  export default {
    components: {
      pub: Pub
    },
    data() {
      return {
        ver_pub: false
      }
    },
  }
</script>

<template>
<!--PONER LINKS Y NOMBRE Y HORA -->
 <div id="todo">
  <div v-if="ver_pub==false">
    <div id="contenedor">
            <div id="central">
                <div id="login">
                    <div class="titulo">
                        Bienvenido
                    </div>
                    <form v-on:submit.prevent="ver_pub=true" id="loginform">
                        <input type="text" name="usuario" placeholder="Usuario" required>
                        
                        <input type="password" placeholder="Contraseña" name="password" required>
                        
                        <button type="submit" title="Ingresar" name="Ingresar">Login</button>
                    </form>
                    <div class="pie-form">
                        <a href="#">¿Perdiste tu contraseña?</a>
                        <a href="#">¿No tienes Cuenta? Registrate</a>
                    </div>
                </div>
                <div class="inferior">
                    <a href="#">Volver</a>
                </div>
            </div>
        </div>
  </div>
  
  <pub v-else ></pub>
  
  <br />
  <button v-if="ver_pub==true"  v-on:click="ver_pub=false" type="submit" class="d-grid gap-2 col-6 mx-auto btn btn-primary opacity-75">Cerrar Sesión</button>
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
 </div>

 
</template>

<style scoped>


  body {
    font-family: 'Overpass', sans-serif;
    font-weight: normal;
    font-size: 100%;
    color: #1b262c;
    margin: 0;
    background-color: #0f4c75;
}

#contenedor {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0;
    padding: 0;
    min-width: 100vw;
    min-height: 100vh;
    width: 100%;
    height: 100%;
}

#central {
    max-width: 320px;
    width: 100%;
}

.titulo {
    font-size: 250%;
    color:#bbe1fa;
    text-align: center;
    margin-bottom: 20px;
}

#login {
    width: 100%;
    padding: 50px 30px;
    background-color: #3282b8;
    
    -webkit-box-shadow: 0px 0px 5px 5px rgba(0,0,0,0.15);
    -moz-box-shadow: 0px 0px 5px 5px rgba(0,0,0,0.15);
    box-shadow: 0px 0px 5px 5px rgba(0,0,0,0.15);
    
    border-radius: 3px 3px 3px 3px;
    -moz-border-radius: 3px 3px 3px 3px;
    -webkit-border-radius: 3px 3px 3px 3px;
    
    box-sizing: border-box;
}

#login input {
    font-family: 'Overpass', sans-serif;
    font-size: 110%;
    color: #1b262c;
    
    display: block;
    width: 100%;
    height: 40px;
    
    margin-bottom: 10px;
    padding: 5px 5px 5px 10px;
    
    box-sizing: border-box;
    
    border: none;
    border-radius: 3px 3px 3px 3px;
    -moz-border-radius: 3px 3px 3px 3px;
    -webkit-border-radius: 3px 3px 3px 3px;
}

#login input::placeholder {
    font-family: 'Overpass', sans-serif;
    color: #E4E4E4;
}

#login button {
    font-family: 'Overpass', sans-serif;
    font-size: 110%;
    color:#1b262c;
    width: 100%;
    height: 40px;
    border: none;
    
    border-radius: 3px 3px 3px 3px;
    -moz-border-radius: 3px 3px 3px 3px;
    -webkit-border-radius: 3px 3px 3px 3px;
    
    background-color: #bbe1fa;
    
    margin-top: 10px;
}

#login button:hover {
    background-color: #0f4c75;
    color:#bbe1fa;
}

.pie-form {
    font-size: 90%;
    text-align: center;    
    margin-top: 15px;
}

.pie-form a {
    display: block;
    text-decoration: none;
    color: #bbe1fa;
    margin-bottom: 3px;
}

.pie-form a:hover {
    color: #0f4c75;
}

.inferior {
    margin-top: 10px;
    font-size: 90%;
    text-align: center;
}

.inferior a {
    display: block;
    text-decoration: none;
    color: #bbe1fa;
    margin-bottom: 3px;
}

.inferior a:hover {
    color: #3282b8;
}

</style>
