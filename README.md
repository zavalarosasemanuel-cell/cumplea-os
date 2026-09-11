<!DOCTYPE html>
<html lang="es">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Feliz Cumpleaños 🦇</title>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {

    min-height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;

    background: aquamarine;

    overflow: hidden;

    transition: background 1s ease;
}


/* =========================
   FONDO BATMAN
========================= */

body.batman {

    background:
        radial-gradient(
            circle at center,
            #3a3a3a 0%,
            #111 45%,
            #000 100%
        );
}


/* =========================
   TARJETA
========================= */

.tarjeta {

    width: 350px;

    padding: 35px;

    background: white;

    border-radius: 20px;

    text-align: center;

    box-shadow:
        0 0 25px rgba(0,0,0,0.4);

    position: relative;

    z-index: 10;
}


.tarjeta h1 {

    font-size: 30px;

    margin-bottom: 15px;
}


.tarjeta p {

    font-size: 18px;

    margin-bottom: 20px;
}


/* =========================
   BOTÓN
========================= */

button {

    padding: 15px 30px;

    border: none;

    border-radius: 12px;

    background: #111;

    color: #ffd900;

    font-size: 18px;

    font-weight: bold;

    cursor: pointer;

    transition: 0.3s;
}


button:hover {

    background: #ffd900;

    color: #000;

    transform: scale(1.08);

    box-shadow:
        0 0 20px #ffd900;
}


/* =========================
   IMÁGENES LATERALES
========================= */

.imagen-fondo {

    position: fixed;

    top: 0;

    width: 340px;

    height: 100vh;

    /*
       FILL hace que la imagen
       ocupe todo el ancho y alto.
    */
    object-fit: fill;

    border-radius: 15px;

    border: 4px solid #ffd900;

    box-shadow:
        0 0 20px #ffd900,
        0 0 40px rgba(255,217,0,0.5);

    z-index: 1;

    display: none;

    opacity: 0.85;

    filter:
        brightness(1.05)
        contrast(1.05);
}


/* =========================
   IZQUIERDA
========================= */

.imagen-izquierda {

    left: 5px;
}


/* =========================
   DERECHA
========================= */

.imagen-derecha {

    right: 5px;
}


/* =========================
   APARICIÓN
========================= */

.imagenes-activas {

    display: block;

    animation:
        aparecerImagen 1.5s ease;
}


@keyframes aparecerImagen {

    from {

        opacity: 0;

        transform: scale(0.85);
    }

    to {

        opacity: 0.85;

        transform: scale(1);
    }
}


/* =========================
   VIDEO
========================= */

#videoContainer {

    display: none;

    position: relative;

    z-index: 5;

    text-align: center;
}


video {

    width: 500px;

    max-width: 70vw;

    max-height: 60vh;

    border-radius: 20px;

    border: 5px solid #ffd900;

    box-shadow:
        0 0 20px #ffd900,
        0 0 50px rgba(255,217,0,0.5);
}


/* =========================
   MENSAJE
========================= */

.mensaje {

    margin-top: 20px;

    font-size: 30px;

    font-weight: bold;

    color: #ffd900;

    text-shadow:
        0 0 5px #000,
        0 0 10px #ffd900,
        0 0 20px #ffd900;
}


/* =========================
   MURCIÉLAGOS
========================= */

.bat {

    position: fixed;

    color: #000;

    font-size: 30px;

    animation:
        volar 6s linear infinite;

    z-index: 2;
}


.bat:nth-child(1) {

    top: 10%;
    left: 10%;
}


.bat:nth-child(2) {

    top: 20%;
    right: 15%;

    animation-delay: 2s;
}


.bat:nth-child(3) {

    bottom: 15%;
    left: 20%;

    animation-delay: 1s;
}


.bat:nth-child(4) {

    bottom: 20%;
    right: 20%;

    animation-delay: 3s;
}


@keyframes volar {

    0% {

        transform:
            translateX(0)
            rotate(0deg);
    }

    50% {

        transform:
            translateX(80px)
            rotate(15deg);
    }

    100% {

        transform:
            translateX(0)
            rotate(0deg);
    }
}


/* =========================
   DESTELLOS
========================= */

.brillo {

    position: fixed;

    color: #ffd900;

    font-size: 25px;

    animation:
        aparecer 2s infinite;

    z-index: 2;
}


.brillo:nth-child(5) {

    top: 15%;
    left: 45%;
}


.brillo:nth-child(6) {

    top: 70%;
    left: 50%;

    animation-delay: 1s;
}


@keyframes aparecer {

    0%, 100% {

        opacity: 0;

        transform: scale(0.5);
    }

    50% {

        opacity: 1;

        transform: scale(1.3);
    }
}


/* =========================
   CELULAR
========================= */

@media (max-width: 700px) {

    .imagen-fondo {

        width: 150px;

        height: 100vh;

        object-fit: fill;

        border-radius: 10px;
    }


    .imagen-izquierda {

        left: -10px;
    }


    .imagen-derecha {

        right: -10px;
    }


    video {

        width: 65vw;

        max-height: 55vh;
    }


    .mensaje {

        font-size: 22px;

        max-width: 70vw;

        margin-left: auto;

        margin-right: auto;
    }
}


/* =========================
   CELULARES PEQUEÑOS
========================= */

@media (max-width: 450px) {

    .imagen-fondo {

        width: 125px;

        height: 100vh;

        opacity: 0.80;

        object-fit: fill;
    }


    .imagen-izquierda {

        left: -15px;
    }


    .imagen-derecha {

        right: -15px;
    }


    video {

        width: 60vw;
    }


    .mensaje {

        font-size: 18px;
    }
}

</style>

</head>


<body>


<!-- TARJETA INICIAL -->

<div class="tarjeta" id="tarjeta">

    <h1>🎁 Sorpresa</h1>

    <p>
        Tengo algo especial para ti...
    </p>

    <button onclick="mostrarVideo()">

        Presiona aquí 💛

    </button>

</div>


<!-- IMAGEN IZQUIERDA -->

<img
    src="3734.jpg.jpeg"
    class="imagen-fondo imagen-izquierda"
    id="imagenIzquierda"
>


<!-- IMAGEN DERECHA -->

<img
    src="3735.jpg.jpeg"
    class="imagen-fondo imagen-derecha"
    id="imagenDerecha"
>


<!-- MURCIÉLAGOS -->

<div class="bat">🦇</div>
<div class="bat">🦇</div>
<div class="bat">🦇</div>
<div class="bat">🦇</div>


<!-- DESTELLOS -->

<div class="brillo">✦</div>
<div class="brillo">✦</div>


<!-- VIDEO -->

<div id="videoContainer">

    <video controls>

        <source
            src="cumple.mp4"
            type="video/mp4"
        >

        Tu navegador no puede reproducir este video.

    </video>


    <div class="mensaje">

        Feliz Cumpleaños Mi Duende Hermosa 💜😛

    </div>

</div>


<script>

function mostrarVideo() {

    /* Activar Batman */

    document.body.classList.add("batman");


    /* Ocultar tarjeta */

    document.getElementById("tarjeta").style.display = "none";


    /* Mostrar imagen izquierda */

    document
        .getElementById("imagenIzquierda")
        .classList.add("imagenes-activas");


    /* Mostrar imagen derecha */

    document
        .getElementById("imagenDerecha")
        .classList.add("imagenes-activas");


    /* Mostrar video */

    document.getElementById("videoContainer").style.display = "block";


    /* Reproducir video */

    const video =
        document.querySelector("#videoContainer video");


    video.play().catch(function() {

        console.log(
            "El navegador requiere presionar Play."
        );

    });

}

</script>


</body>

</html>
