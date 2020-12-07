<template>
    <div class="container">

            <div id="myCarousel" class="carousel slide" data-ride="carousel" data-interval="2500">
          
                <!-- Estructura del carrusel -->
                <ul class="carousel-indicators">
                <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
                <li data-target="#myCarousel" data-slide-to="1"></li>
                <li data-target="#myCarousel" data-slide-to="2"></li>
                <li data-target="#myCarousel" data-slide-to="3"></li>
                </ul>
                
                <!-- Tamaño y origne de las imágenes -->
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="../assets/Banner_NSC00.jpg" alt="Banner" width="1200" height="300">
                        <div class="carousel-caption">
                            <h3> SOLUCIONES A SU MEDIDA</h3>
                            <p>Encuentre con nosotros todo lo que necesite</p>
                        </div>   
                    </div>
                    <div class="carousel-item">
                        <img src="../assets/Banner_NSC01.jpg" alt="Chicago" width="1200" height="300">
                        <div class="carousel-caption">
                            <h3> BUSQUE INFORMACION BENEFICIOSA</h3>
                            <p>Encuentre con nosotros cómo mejorar su bienestar</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="../assets/Banner_NSC02.jpg" alt="New York" width="1200" height="300">
                        <div class="carousel-caption">
                            <h3> PRODUCTOS NATURALES A SU MANO</h3>
                            <p>De la naturaleza para su bienestar</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="../assets/Banner_NSC03.jpg" alt="New York" width="1200" height="300">
                        <div class="carousel-caption">
                            <h3> NOS AJUSTAMOS A SUS NECESIDADES</h3>
                            <p>Viva plenamente sin preocupaciones</p>
                        </div>
                    </div>
                </div>
                
                <!-- Controles de derecha e izquierda -->
                <a class="carousel-control-prev" href="#myCarousel" data-slide="prev">
                <span class="carousel-control-prev-icon"></span>
                </a>
                <a class="carousel-control-next" href="#myCarousel" data-slide="next">
                <span class="carousel-control-next-icon"></span>
                </a>
          </div>
          
          </div>  

</template>

<script> 
export default {
    name: 'CarouselHeader',
}
</script>