<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>CHEZ FLEUR - Parfums & Bébé</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    /* Reset & font */
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: url('https://images.unsplash.com/photo-1504196606672-aef5c9cefc92?auto=format&fit=crop&w=1500&q=80') no-repeat center center fixed;
      background-size: cover;
      color: #4d2c3d;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      animation: fadeInBg 3s ease forwards;
    }
    @keyframes fadeInBg {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    header {
      background: #ff66b2;
      color: white;
      padding: 2rem 1rem;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      position: relative;
      user-select: none;
    }
    header h1 {
      font-size: 3rem;
      margin: 0;
      letter-spacing: 2px;
      text-shadow: 1px 1px 3px #900046;
    }
    header p {
      font-size: 1.3rem;
      margin-top: 0.4rem;
      font-weight: 500;
    }
    header::before {
      content: "";
      position: absolute;
      top: 1rem;
      left: 1rem;
      background-image: url('https://cdn-icons-png.flaticon.com/512/3041/3041127.png');
      background-size: contain;
      width: 50px;
      height: 50px;
      background-repeat: no-repeat;
      filter: drop-shadow(1px 1px 2px #600034);
    }

    main {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      padding: 2rem;
      flex-grow: 1;
      max-width: 1200px;
      margin: auto;
      animation: fadeInUp 1.5s ease forwards;
    }
    @keyframes fadeInUp {
      from {opacity: 0; transform: translateY(40px);}
      to {opacity: 1; transform: translateY(0);}
    }

    .product-card {
      background: white;
      border-radius: 15px;
      padding: 1rem;
      box-shadow: 0 8px 25px rgba(255, 102, 178, 0.3);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
      position: relative;
      overflow: hidden;
    }
    .product-card:hover {
      transform: translateY(-10px) scale(1.05);
      box-shadow: 0 20px 40px rgba(255, 102, 178, 0.5);
    }
    .product-card img {
      width: 100%;
      border-radius: 10px;
      height: 220px;
      object-fit: cover;
      transition: filter 0.3s ease;
    }
    .product-card:hover img {
      filter: brightness(1.1);
    }
    .product-card h3 {
      margin: 1rem 0 0.5rem;
      color: #cc2b80;
      font-weight: 700;
      font-size: 1.4rem;
    }
    .price {
      color: #ff3399;
      font-size: 1.2rem;
      font-weight: bold;
      margin-bottom: 0.5rem;
    }
    .whatsapp-btn {
      background-color: #ff3399;
      color: white;
      border: none;
      padding: 0.7rem 1.5rem;
      border-radius: 30px;
      text-decoration: none;
      display: inline-block;
      font-weight: 700;
      transition: background 0.3s ease;
      box-shadow: 0 5px 12px rgba(255, 51, 153, 0.4);
    }
    .whatsapp-btn:hover {
      background-color: #e60073;
      box-shadow: 0 7px 15px rgba(230, 0, 115, 0.7);
    }

    .order-form {
      background-color: #fff0f6;
      padding: 2rem;
      max-width: 600px;
      margin: 3rem auto 4rem auto;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(255, 102, 178, 0.3);
      animation: fadeIn 2s ease forwards;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    .order-form h2 {
      text-align: center;
      color: #cc2b80;
      margin-bottom: 1rem;
      font-weight: 700;
      letter-spacing: 1.2px;
    }
    .order-form input,
    .order-form select,
    .order-form textarea {
      width: 100%;
      padding: 0.9rem;
      margin: 0.7rem 0;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-family: 'Poppins', sans-serif;
      font-size: 1rem;
      transition: border-color 0.3s ease;
      resize: vertical;
    }
    .order-form input:focus,
    .order-form select:focus,
    .order-form textarea:focus {
      border-color: #ff66b2;
      outline: none;
      box-shadow: 0 0 8px #ff66b2;
    }
    .order-form button {
      width: 100%;
      background-color: #ff66b2;
      color: white;
      padding: 1rem;
      font-size: 1.15rem;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 700;
      transition: background 0.3s ease;
      box-shadow: 0 5px 15px rgba(255, 102, 178, 0.5);
    }
    .order-form button:hover {
      background-color: #e60073;
      box-shadow: 0 7px 20px rgba(230, 0, 115, 0.7);
    }

    .about-section {
      background-image: url('https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?auto=format&fit=crop&w=1500&q=80');
      background-size: cover;
      background-position: center;
      color: white;
      padding: 4rem 2rem;
      text-align: center;
      max-width: 900px;
      margin: 2rem auto;
      border-radius: 15px;
      box-shadow: 0 0 25px rgba(255, 102, 178, 0.6);
      animation: fadeIn 2.5s ease forwards;
    }
    .about-section h2 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      letter-spacing: 1.3px;
      text-shadow: 2px 2px 6px #900046;
    }
    .about-section p {
      font-size: 1.3rem;
      line-height: 1.6;
      background-color: rgba(255, 102, 178, 0.75);
      padding: 1.5rem;
      border-radius: 15px;
      max-width: 700px;
      margin: auto;
      box-shadow: 0 0 12px rgba(204, 43, 128, 0.8);
      user-select: text;
    }

    footer {
      background: #ff66b2;
      color: white;
      text-align: center;
      padding: 1.5rem;
      margin-top: auto;
      font-weight: 600;
      letter-spacing: 1px;
      box-shadow: 0 -4px 12px rgba(0,0,0,0.15);
      user-select: none;
    }

    /* Responsive */
    @media (max-width: 600px) {
      header h1 {
        font-size: 2.2rem;
      }
      main {
        padding: 1rem;
        grid-template-columns: 1fr;
      }
      .order-form {
        margin: 2rem 1rem;
        padding: 1.5rem;
      }
    }
  </style>
</head>
<body>

  <!-- Musique douce de fond -->
  <audio autoplay loop controls style="position: fixed; bottom: 10px; right: 10px; width: 200px; opacity: 0.8; border-radius: 10px;">
    <source src="https://cdn.pixabay.com/audio/2022/12/11/audio_99fc515ae8.mp3" type="audio/mpeg" />
    Ton navigateur ne supporte pas l'audio.
  </audio>

  <header>
    <h1>CHEZ FLEUR</h1>
    <p>Parfums & Vêtements pour bébé - Livraison rapide</p>
  </header>

  <main>
    <div class="product-card" tabindex="0">
      <img src="https://images.unsplash.com/photo-1611599531378-4b4ad78294e2?auto=format&fit=crop&w=500&q=80" alt="Parfum Élégant" />
      <h3>Parfum Élégant</h3>
      <p class="price">5000 FCFA</p>
      <a class="whatsapp-btn" href="https://wa.me/225710496467?text=Je souhaite commander le Parfum Élégant" target="_blank" rel="noopener noreferrer">Commander via WhatsApp</a>
    </div>

    <div class="product-card" tabindex="0">
      <img src="https://images.unsplash.com/photo-1617181514165-3fc902bba1cc?auto=format&fit=crop&w=500&q=80" alt="Tenue Bébé Fille" />
      <h3>Tenue Bébé Fille</h3>
      <p class="price">5000 FCFA</p>
      <a class="whatsapp-btn" href="https://wa.me/225710496467?text=Je souhaite commander la Tenue Bébé Fille" target="_blank" rel="noopener noreferrer">Commander via WhatsApp</a>
    </div>

    <div class="product-card" tabindex="0">
      <img src="https://images.unsplash.com/photo-1604335399108-6719787b13e2?auto=format&fit=crop&w=500&q=80" alt="Tenue Bébé Garçon" />
      <h3>Tenue Bébé Garçon</h3>
      <p class="price">5000 FCFA</p>
      <a class="whatsapp-btn" href="https://wa.me/225710496467?text=Je souhaite commander la Tenue Bébé Garçon" target="_blank" rel="noopener noreferrer">Commander via WhatsApp</a>
    </div>
  </main>

  <section class="order-form" aria-label="Formulaire de commande">
    <h2>Passer une commande</h2>
    <form action="https://api.whatsapp.com/send" method="get" target="_blank" onsubmit="return prepareWhatsAppMessage(event)">
      <input type="hidden" name="phone" value="225710496467" />
      <input type="text" name="Nom" placeholder="Votre nom" required aria-required="true" />
      <select name="Produit" required aria-required="true">
        <option value="" disabled selected>Choisissez un produit</option>
        <option value="Parfum Élégant">Parfum Élégant</option>
        <option value="Tenue Bébé Fille">Tenue Bébé Fille</option>
        <option value="Tenue Bébé Garçon">Tenue Bébé Garçon</option>
      </select>
      <input type="number" name="Quantité" placeholder="Quantité" min="1" required aria-required="true" />
      <textarea name="Message" placeholder="Message supplémentaire (facultatif)" rows="3"></textarea>
      <button type="submit">Envoyer via WhatsApp</button>
    </form>
  </section>

  <section class="about-section" aria-label="Message de Fleur">
    <h2>Message de Fleur</h2>
    <p>
      Merci de soutenir notre boutique ! Nous sélectionnons avec soin nos produits pour vos bébés et vos moments parfumés. Commandez en toute confiance !
    </p>
  </section>

  <footer>
    <p>Contact WhatsApp : 07 10 49 64 67 | CHEZ FLEUR © 2025</p>
  </footer>

  <script>
    function prepareWhatsAppMessage(event) {
      event.preventDefault();
      const form = event.target;
      const nom = form.Nom.value.trim();
      const produit = form.Produit.value;
      const quantite = form.Quantité.value;
      const messageSup = form.Message.value.trim();

      let message = `Bonjour, je m'appelle ${nom}.\nJe souhaite commander ${quantite} x ${produit}.`;
      if (messageSup) {
        message += `\nMessage : ${messageSup}`;
      }
      const phone = form.phone.value;
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
      window.open(url, '_blank');
      return false;
    }
  </script>
</body>
</html>

