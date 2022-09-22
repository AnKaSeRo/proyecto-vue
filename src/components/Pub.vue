<script>
import Pefil from './Pefil.vue';
    export default {
      components: {
      perfil: Pefil
    },
    name: "App",
    data() {
        return {
            nombre: "",
            pub: "",
            img: "",
            fecha: "",
            publicaciones: [],
            ver_perfil:false
        };
    },
    methods: {
        guardarPublicacion() {
            this.publicaciones.push({
                nombre: this.nombre,
                pub: this.pub,
                img: this.img,
                fecha: new Date().toLocaleTimeString()
            });
            this.nombre = "";
            this.pub = "";
            this.img = "";
            console.log(this.publicaciones);
        },
    },
    components: { Pefil }
};
</script>
  
  <template>

<div v-if="ver_perfil==false">
    <div>
        <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <form action="" v-on:submit.prevent="guardarPublicacion"> 
        <br />
        <br />

        <div id="pub" class="d-grid gap-2 col-6 mx-auto">

          
        <div>
          <svg xmlns="http://www.w3.org/2000/svg" class="text-center d-grid gap-2 col-6 mx-auto icon icon-tabler icon-tabler-user" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <circle cx="12" cy="7" r="4" />
            <path d="M6 21v-2a4 4 0 0 1 4 -4h4a4 4 0 0 1 4 4v2" />
          </svg>
        </div>
            <div  id="contenedorDeIn">


              <div>
                <div class="input-group mb-3">
    <span class="input-group-text" id="basic-addon1">@</span>
    <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1" v-model="nombre">
</div>

<br/>

  <div class="input-group">
      <span class="input-group-text">¿Cómo te sientes hoy?</span>
      <textarea class="form-control" aria-label="With textarea" v-model="pub"></textarea>
    </div>
    <br/>
    <br/>

    <div class="input-group mb-3">
      <span class="input-group-text" id="basic-addon1">Pon una imagen</span>
      <input type="text" class="form-control" aria-label="Username" aria-describedby="basic-addon1" v-model="img">
  </div>
<br/>



          </div>
           
          </div>
      </div>
      <br />
      <br />
      <br />
      <button class="btn btn-primary opacity-75 d-grid gap-2 col-6 mx-auto" type="submit" value="Input" >Publicar</button>
      <br />
      
    </form>
    </div>

    <div >
      <div id="resultado" v-for="Publicacion of publicaciones" class="card text-center d-grid gap-2 col-6 mx-auto">
          <div class="card-header">
            {{Publicacion.nombre}}
          </div>
          <div class="card-body">
            <br />
            <p class="card-text">
              {{Publicacion.pub}}
              <img v-bind:src="Publicacion.img" alt="">
            </p>
            <br />
          </div>
          <div class="card-footer text-muted">
            {{Publicacion.fecha}}
          </div>
        </div>
      </div>





  <nav id="nav" class="navbar navbar-dark bg-primary opacity-75 fixed-top">

  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-alien" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
        <path d="M11 17a2.5 2.5 0 0 0 2 0" />
        <path d="M12 3c-4.664 0 -7.396 2.331 -7.862 5.595a11.816 11.816 0 0 0 2 8.592a10.777 10.777 0 0 0 3.199 3.064c1.666 1 3.664 1 5.33 0a10.777 10.777 0 0 0 3.199 -3.064a11.89 11.89 0 0 0 2 -8.592c-.466 -3.265 -3.198 -5.595 -7.862 -5.595z" />
        <line x1="8" y1="11" x2="10" y2="13" />
        <line x1="16" y1="11" x2="14" y2="13" />
    </svg>
    </a>

    <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasDarkNavbar" aria-controls="offcanvasDarkNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="offcanvas offcanvas-end text-bg-primary" tabindex="-1" id="offcanvasDarkNavbar" aria-labelledby="offcanvasDarkNavbarLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasDarkNavbarLabel">Menú</h5>
        <button type="button" class="btn-close btn-close-white" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">
              Home
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-smart-home" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                <path d="M19 8.71l-5.333 -4.148a2.666 2.666 0 0 0 -3.274 0l-5.334 4.148a2.665 2.665 0 0 0 -1.029 2.105v7.2a2 2 0 0 0 2 2h12a2 2 0 0 0 2 -2v-7.2c0 -.823 -.38 -1.6 -1.03 -2.105" />
                <path d="M16 15c-2.21 1.333 -5.792 1.333 -8 0" />
              </svg>
            </a>
          </li>
          <br/>
          <br/>
          <li class="nav-item">

              <a v-on:click="ver_perfil=true" class="nav-link active" aria-current="page">
                Perfil
                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-id" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
                  <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                  <rect x="3" y="4" width="18" height="16" rx="3" />
                  <circle cx="9" cy="10" r="2" />
                  <line x1="15" y1="8" x2="17" y2="8" />
                  <line x1="15" y1="12" x2="17" y2="12" />
                  <line x1="7" y1="16" x2="17" y2="16" />
                </svg>
              </a>
            
          </li>
          <br/>
          <br/>
        </ul>
        <br/>
        <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </div>
</nav>

</div>

<div v-else>
  <div class="nav-bg">
        <nav class="navegacion-principal contenedor">
            <a class="enlace1" href="#"></a>
            <a class="enlace2" href="#"></a>
        </nav>	
    </div>

    
    
    <div class="container">
       
        <div class="d-flex justify-content-center">
          <div class="">
            <img class="foto" src="https://th.bing.com/th/id/OIP.0lcuAsQ0V1GwktjPc0SUlgHaG4?pid=ImgDet&rs=1"/>
            <p>Alumno: Andrea Karina Serrano Rodríguez</p>
            <p>Matricula: 1994424 </p>
            <p>Carrera: ITS</p>
            <p>Agosto –Diciembre 2022</p>
            
        </div>
        </div>

    </div>
    
    <br/>
   <br/>
   <br/>
   <br/>

   
   <footer class="text-center">
        <p>Todos los derechos reservados. Andrea Karina Serrano Rdz</p>
    </footer>
    
</div>
<button v-if="ver_perfil==true"  v-on:click="ver_perfil=false" type="submit" class="d-grid gap-2 col-6 mx-auto btn btn-primary opacity-75">Regresar</button>
  




    
</template>
