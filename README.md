<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Menthe au Lait Chez Moya</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500;700&display=swap" rel="stylesheet" />
  <style>
    /* Reset */
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(135deg, #d0f0c0, #ffe680, #ffb347);
      color: #2b3a2b;
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      background: linear-gradient(90deg, #3ac9a9, #f7dc6f);
      padding: 2.5rem 1rem;
      text-align: center;
      box-shadow: 0 5px 15px rgba(0,0,0,0.15);
      color: #1b3a2a;
    }
    header h1 {
      margin: 0;
      font-size: 2.8rem;
      font-weight: 700;
      text-shadow: 1px 1px 2px #f9f9f9;
    }
    header p {
      margin: 0.5rem 0 0;
      font-size: 1.3rem;
      font-weight: 500;
      text-shadow: 1px 1px 1px #f9f9f9;
    }

    main {
      flex: 1;
      max-width: 1000px;
      margin: 2.5rem auto;
      padding: 0 1rem;
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(300px,1fr));
      gap: 2.5rem;
    }

    .product-card {
      background: #ffffffcc;
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(255, 167, 38, 0.3);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 1.5rem;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border: 3px solid #3ac9a9;
    }
    .product-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 35px rgba(255, 167, 38, 0.6);
      border-color: #f7dc6f;
    }
    .product-card img {
      width: 100%;
      border-radius: 20px;
      margin-bottom: 1.2rem;
      object-fit: cover;
      height: 220px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    .product-card h3 {
      margin: 0.5rem 0 0.3rem;
      color: #3a7d44;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .product-card p.description {
      flex-grow: 1;
      color: #4b6f32;
      font-size: 1.1rem;
      margin-bottom: 1rem;
      text-align: center;
      font-weight: 500;
    }
    .price {
      font-weight: 700;
      font-size: 1.3rem;
      margin-bottom: 1.3rem;
      color: #d2691e;
      text-shadow: 1px 1px 1px #fff3e0;
    }
    .whatsapp-btn {
      background-color: #25D366;
      color: white;
      padding: 14px 32px;
      border: none;
      border-radius: 25px;
      font-weight: 700;
      font-size: 1.2rem;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      box-shadow: 0 6px 12px rgba(37, 211, 102, 0.5);
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
    }
    .whatsapp-btn:hover {
      background-color: #1aa34a;
      box-shadow: 0 8px 18px rgba(26, 163, 74, 0.8);
    }

    form {
      grid-column: 1 / -1;
      background: #fff4cccc;
      padding: 2.5rem 2rem;
      border-radius: 25px;
      box-shadow: 0 12px 30px rgba(255, 167, 38, 0.4);
      color: #4b6f32;
      max-width: 600px;
      margin: 0 auto 3rem;
      font-weight: 600;
    }
    form h2 {
      margin-top: 0;
      color: #e57c23;
      margin-bottom: 1.8rem;
      text-align: center;
      font-weight: 800;
      letter-spacing: 1.2px;
      text-transform: uppercase;
    }
    form label {
      display: block;
      margin: 1rem 0 0.5rem;
      font-weight: 600;
      color: #3a7d44;
      font-size: 1rem;
    }
    form input, form select {
      width: 100%;
      padding: 14px 18px;
      margin-bottom: 10px;
      border-radius: 15px;
      border: 2px solid #a6cf88;
      outline: none;
      font-size: 1.1rem;
      background: #f9f9f9;
      color: #2b3a2b;
      transition: border-color 0.3s ease;
    }
    form input:focus, form select:focus {
      border-color: #3ac9a9;
      background: #e0f7ef;
    }
    form button {
      margin-top: 1.5rem;
      width: 100%;
      padding: 16px 20px;
      background: linear-gradient(45deg, #ff9800, #ffb347);
      color: #3a7d44;
      font-weight: 800;
      font-size: 1.3rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(255, 145, 0, 0.6);
      transition: background 0.4s ease;
    }
    form button:hover {
      background: linear-gradient(45deg, #e57c23, #f7dc6f);
      box-shadow: 0 10px 28px rgba(255, 164, 0, 0.9);
    }

    footer {
      background: #f7dc6f;
      text-align: center;
      color: #3a7d44;
      padding: 1.8rem 1rem;
      font-size: 1.1rem;
      font-weight: 700;
      box-shadow: 0 -4px 10px rgba(0,0,0,0.1);
      letter-spacing: 0.05em;
      text-transform: uppercase;
    }

    @media (max-width: 480px) {
      header h1 {
        font-size: 2rem;
      }
      main {
        margin: 1rem;
        grid-template-columns: 1fr;
      }
      .product-card img {
        height: 200px;
      }
      form {
        padding: 1.8rem 1.2rem;
      }
      form button {
        font-size: 1.1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Menthe au Lait Chez Moya</h1>
    <p>Des boissons fraîches, naturelles et pleines de saveurs ! 🍹🌿</p>
  </header>

  <main>
    <div class="product-card">
      <img src="https://images.unsplash.com/photo-1571079942084-7a6b4f0d7b11?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=60" alt="Menthe au Lait" />
      <h3>Menthe au Lait</h3>
      <p class="description">Cocktail au lait et menthe - goût naturel, très rafraîchissant.</p>
      <p class="price">Prix : 1000 F CFA</p>
      <a href="https://wa.me/2250712043691" target="_blank" class="whatsapp-btn">📲 Commander sur WhatsApp</a>
    </div>

    <div class="product-card">
      <img src="https://images.unsplash.com/photo-1572441710534-386757ad2471?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=60" alt="Cocktail Fruit" />
      <h3>Cocktail Fruité</h3>
      <p class="description">Cocktail fruité - mangue, ananas, citron. 100% naturel 🍍🥭</p>
      <p class="price">Prix : 1500 F CFA</p>
      <a href="https://wa.me/2250712043691" target="_blank" class="whatsapp-btn">📲 Commander sur WhatsApp</a>
    </div>

    <form>
      <h2>📦 Passer une commande</h2>
      <label for="name">Nom complet</label>
      <input id="name" type="text" placeholder="Votre nom" required />
      <label for="phone">Téléphone</label>
      <input id="phone" type="tel" placeholder="Votre numéro" required />
      <label for="address">Quartier / Adresse</label>
      <input id="address" type="text" placeholder="Votre adresse de livraison" required />
      <label for="product">Choisissez un cocktail</label>
      <select id="product" required>
        <option value="">-- Sélectionnez --</option>
        <option value="Menthe au Lait">Menthe au Lait</option>
        <option value="Cocktail Fruité">Cocktail Fruité</option>
      </select>
      <button type="submit">Envoyer la commande</button>
    </form>
  </main>

  <footer>
    <p>📞 Contact WhatsApp : 07 120 436 91 — Livraison à Abidjan</p>
  </footer>
</body>
</html>
