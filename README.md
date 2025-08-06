<!DOCTYPE html><html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Boda de Ana & Pablo</title>
  <style>
    body {
      margin: 0;
      font-family: 'Georgia', serif;
      background-color: #f5f1ea;
      color: #4e342e;
    }
    header {
      background-color: #d7ccc8;
      padding: 60px 20px;
      text-align: center;
    }
    header h1 {
      font-size: 3em;
      margin: 0;
    }
    header p {
      font-size: 1.2em;
      margin-top: 10px;
    }
    section {
      padding: 40px 20px;
      max-width: 800px;
      margin: auto;
    }
    .countdown {
      font-size: 2em;
      text-align: center;
      margin-top: 20px;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 10px;
      margin-top: 20px;
    }
    .gallery img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
    }
    footer {
      background-color: #a1887f;
      color: white;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Ana & Pablo</h1>
    <p>¡Nos casamos! 6 de septiembre del 2025 - Pazo de Miradores</p>
    <div class="countdown" id="countdown"></div>
  </header>  <section>
    <h2>Nuestra historia</h2>
    <p>
      Desde el primer momento en que nos cruzamos, supimos que algo especial estaba por comenzar. Con cada paso, cada aventura y cada risa, hemos construido una historia única, y ahora queremos celebrarla con ustedes.
    </p>
  </section>  <section>
    <h2>Detalles del evento</h2>
    <p><strong>📍 Lugar:</strong> Pazo de Miradores</p>
    <p><strong>📅 Fecha:</strong> Sábado, 6 de septiembre del 2025</p>
    <p><strong>🕓 Hora:</strong> 17:00 hrs</p>
    <p><strong>🎩 Código de vestimenta:</strong> Formal / Cóctel</p>
  </section>  <section>
    <h2>Galería</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/400x300?text=Foto+1" alt="Galería 1" />
      <img src="https://via.placeholder.com/400x300?text=Foto+2" alt="Galería 2" />
      <img src="https://via.placeholder.com/400x300?text=Foto+3" alt="Galería 3" />
      <img src="https://via.placeholder.com/400x300?text=Foto+4" alt="Galería 4" />
    </div>
  </section>  <footer>
    Con amor, Ana & Pablo ❤️
  </footer>  <script>
    // Cuenta regresiva
    const countdown = document.getElementById("countdown");
    const eventDate = new Date("2025-09-06T17:00:00").getTime();

    const updateCountdown = () => {
      const now = new Date().getTime();
      const diff = eventDate - now;

      if (diff < 0) {
        countdown.innerHTML = "¡Ya estamos celebrando!";
        return;
      }

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / 1000 / 60) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      countdown.innerHTML = `Faltan ${days} días, ${hours}h ${minutes}m ${seconds}s`;
    };

    setInterval(updateCountdown, 1000);
  </script></body>
</html>