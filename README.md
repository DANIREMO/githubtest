<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para ti ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: url("fondo.jpg") no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      text-align: center;
      overflow-x: hidden;
      position: relative;
    }

    /* Fondo semitransparente */
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.5);
      z-index: -1;
    }

    section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 2rem;
      text-align: center;
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }

    p {
      max-width: 700px;
      margin-bottom: 1rem;
      line-height: 1.8;
      font-size: 1.3rem;
    }

    button {
      background: #ff6f61;
      border: none;
      color: white;
      padding: 1rem 2rem;
      margin: 0.5rem;
      border-radius: 12px;
      font-size: 1.3rem;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #e65100;
    }

    .hidden {
      display: none;
    }

    .fireworks {
      font-size: 4rem;
      margin: 1rem 0;
      animation: pop 1s infinite alternate;
    }

    @keyframes pop {
      from { transform: scale(1); }
      to { transform: scale(1.2); }
    }

    /* Carrusel */
    .carousel {
      position: relative;
      width: 80%;
      max-width: 500px;
      overflow: hidden;
      border-radius: 15px;
      margin-bottom: 1rem;
    }

    .carousel img {
      width: 100%;
      display: none;
      border-radius: 15px;
    }

    .carousel img.active {
      display: block;
    }

    /* Collage centrado 2x2 */
    .collage {
      display: grid;
      grid-template-columns: repeat(2, 200px); /* 2 columnas */
      grid-template-rows: repeat(2, 200px);    /* 2 filas */
      justify-content: center; /* centra horizontalmente */
      gap: 10px;
      margin: 1rem auto;
    }

    .collage img {
      width: 100%;
      height: 100%;
      object-fit: cover; /* mantiene proporción */
      border-radius: 10px;
    }

    /* Responsivo */
    @media (max-width: 600px) {
      h1 { font-size: 2.2rem; }
      h2 { font-size: 1.6rem; }
      p { font-size: 1.1rem; }
      button { font-size: 1.1rem; }
      .collage {
        grid-template-columns: repeat(2, 45%); /* columnas más pequeñas */
        grid-template-rows: auto; /* filas automáticas */
      }
    }
  </style>
</head>
<body>

  <!-- Pantalla 1 -->
  <section id="pantalla1">
    <h1>Holiii mi amooor ✨</h1>
    <p>Hice este pequeño espacio solo para ti, porque hay algo especial que quiero decirte...</p>
    <button onclick="mostrarPantalla(2)">Haz clic para empezar 💫</button>
  </section>

  <!-- Pantalla 2 -->
  <section id="pantalla2" class="hidden">
    <h2>Lo que me encanta de ti 💕</h2>
    <p>• Tus ojitos bonitos.<br>
       • Siempre me haces sentir acompañado, aunque estemos lejos.<br>
       • Tu cabello todo precioso.<br>
       • Jugar al forcho contigo.<br>
       • Todo tu cuerpo es espectacular.<br>
       • Me fascina tu forma de ser.<br>
       • Me haces feliz con las cosas más simples.</p>
    <button onclick="mostrarPantalla(3)">Siguiente ➡️</button>
  </section>

  <!-- Pantalla 3 -->
  <section id="pantalla3" class="hidden">
    <h2>No tenemos muchos momentos, pero los que estoy contigo los disfruto muchooooo!!! 📸</h2>
    <div class="carousel">
      <img src="foto1.jpg" alt="Recuerdo 1" class="active">
      <img src="foto2.jpg" alt="Recuerdo 2">
      <img src="foto3.jpg" alt="Recuerdo 3">
      <img src="foto4.jpg" alt="Recuerdo 4">
    </div>
    <p>Aunque la distancia esté de por medio, cada momento contigo tiene un valor infinito.</p>
    <button onclick="mostrarPantalla(4)">Siguiente ➡️</button>
  </section>

  <!-- Pantalla 4 -->
  <section id="pantalla4" class="hidden">
    <h2>❤️ Lo que siento por ti ❤️</h2>
    <p>Con el tiempo me he dado cuenta de que lo que siento por ti no es pasajero.<br>
       Me inspiras, me haces feliz y me ilusiona pensar en todo lo que podemos construir juntos.<br>
       Aquí abajo unas fotitos de nosotros JKASDKJADKJASJ.</p>
    <div class="collage">
      <img src="foto5.jpg" alt="Collage 1">
      <img src="foto6.jpg" alt="Collage 2">
      <img src="foto7.jpg" alt="Collage 3">
      <img src="foto8.jpg" alt="Collage 4">
    </div>
    <button onclick="mostrarPantalla(5)">Siguiente ➡️</button>
  </section>

  <!-- Pantalla 5 -->
  <section id="pantalla5" class="hidden">
    <h1>Ahora sí lo importante y perdón por ser tan friki</h1>
    <div class="fireworks">✨🎇✨</div>
    <h2>Jessi... ¿Quieres ser mi novia? 💖</h2>
    <button onclick="mostrarPantalla(6)">¡Sí, obvio! 😍</button>
    <button onclick="mostrarPantalla(6)">Claro que sí 🥰</button>
    <button onclick="mostrarPantalla(6)">Por supuesto 💕</button>
  </section>

  <!-- Pantalla final -->
  <section id="pantalla6" class="hidden">
    <h1>💌 Gracias por decir que sí 💌</h1>
    <p>Gracias por ser tú, por estar en mi vida y por darme razones para sonreír cada día.<br>
       Pase lo que pase, siempre te voy a elegir ❤️</p>
  </section>

  <script>
    // Cambiar pantallas
    function mostrarPantalla(num) {
      document.querySelectorAll("section").forEach(s => s.classList.add("hidden"));
      document.getElementById("pantalla" + num).classList.remove("hidden");
    }

    // Carrusel automático
    let index = 0;
    const images = document.querySelectorAll(".carousel img");
    setInterval(() => {
      images[index].classList.remove("active");
      index = (index + 1) % images.length;
      images[index].classList.add("active");
    }, 2500);
  </script>

</body>
</html>
