<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>El Fogón de la Huancaina | Sabor que enamora</title>
  <!-- Bootstrap 5 -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" />
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800;900&family=Playfair+Display:wght@700;900&display=swap" rel="stylesheet" />
  <style>
    :root {
      --primary: #D84A2A;
      --secondary: #F9A03F;
      --dark: #2C1A0E;
      --light: #FFF8F0;
      --gold: #E6B84C;
      --facebook: #1877f2;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Montserrat', sans-serif;
      background-color: var(--light);
      color: var(--dark);
      overflow-x: hidden;
    }
    h1, h2, h3, h4, h5 {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
    }
    .navbar {
      background-color: var(--dark) !important;
      box-shadow: 0 4px 15px rgba(0,0,0,0.4);
    }
    .navbar-brand {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      font-weight: 900;
      color: var(--gold) !important;
      letter-spacing: 1px;
    }
    .navbar-brand span { color: var(--secondary); }
    .nav-link {
      color: white !important;
      font-weight: 600;
      margin: 0 8px;
      transition: 0.3s;
    }
    .nav-link:hover { color: var(--gold) !important; }
    .btn-primary-custom {
      background: var(--primary);
      border: none;
      color: white;
      font-weight: 800;
      padding: 14px 36px;
      border-radius: 50px;
      transition: all 0.3s;
      box-shadow: 0 6px 20px rgba(216,74,42,0.4);
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .btn-primary-custom:hover {
      background: #B33A1F;
      transform: scale(1.05) translateY(-3px);
      color: white;
      box-shadow: 0 10px 30px rgba(216,74,42,0.6);
    }
    .btn-gold {
      background: var(--gold);
      border: none;
      color: var(--dark);
      font-weight: 800;
      padding: 14px 36px;
      border-radius: 50px;
      transition: 0.3s;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .btn-gold:hover {
      background: #d4a33b;
      transform: scale(1.05) translateY(-3px);
      box-shadow: 0 10px 30px rgba(230,184,76,0.4);
    }
    .btn-facebook {
      background: var(--facebook);
      border: none;
      color: white;
      font-weight: 800;
      padding: 14px 36px;
      border-radius: 50px;
      transition: 0.3s;
      box-shadow: 0 6px 20px rgba(24,119,242,0.4);
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .btn-facebook:hover {
      background: #0d65d9;
      transform: scale(1.05) translateY(-3px);
      color: white;
      box-shadow: 0 10px 30px rgba(24,119,242,0.6);
    }
    .btn-whatsapp-lg {
      background: #25D366;
      border: none;
      color: white;
      font-weight: 800;
      padding: 16px 48px;
      border-radius: 50px;
      font-size: 1.4rem;
      box-shadow: 0 8px 30px rgba(37,211,102,0.5);
      transition: 0.3s;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .btn-whatsapp-lg:hover {
      background: #1da851;
      transform: scale(1.05) translateY(-3px);
      color: white;
      box-shadow: 0 12px 40px rgba(37,211,102,0.7);
    }
    .hero {
      background: linear-gradient(135deg, rgba(44,26,14,0.88), rgba(44,26,14,0.75)),
                  url('https://images.unsplash.com/photo-1555939594-58d7cb561ad1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
      min-height: 90vh;
      display: flex;
      align-items: center;
      text-align: center;
      color: white;
      padding: 2rem 0;
    }
    .hero h1 {
      font-size: 4.8rem;
      text-shadow: 4px 4px 15px rgba(0,0,0,0.8);
    }
    .hero p { font-size: 1.6rem; text-shadow: 2px 2px 10px rgba(0,0,0,0.8); }
    .section-title {
      position: relative;
      display: inline-block;
      margin-bottom: 2.5rem;
      font-size: 3rem;
    }
    .section-title::after {
      content: '';
      position: absolute;
      bottom: -12px;
      left: 50%;
      transform: translateX(-50%);
      width: 120px;
      height: 5px;
      background: var(--gold);
      border-radius: 10px;
    }
    .menu-card {
      border: none;
      border-radius: 20px;
      background: white;
      box-shadow: 0 8px 25px rgba(0,0,0,0.08);
      transition: all 0.3s;
      height: 100%;
      padding: 1.5rem;
      position: relative;
      overflow: hidden;
    }
    .menu-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 18px 45px rgba(0,0,0,0.15);
    }
    .menu-card .icon {
      font-size: 2.8rem;
      color: var(--primary);
      margin-bottom: 0.8rem;
    }
    .menu-card h5 {
      font-family: 'Playfair Display', serif;
      color: var(--dark);
      font-weight: 700;
      font-size: 1.3rem;
    }
    .menu-card .precio {
      font-weight: 800;
      color: var(--primary);
      font-size: 1.3rem;
    }
    .menu-card .desc { color: #555; font-size: 0.95rem; }
    .badge-day {
      background: var(--gold);
      color: var(--dark);
      font-weight: 800;
      padding: 10px 28px;
      border-radius: 50px;
      font-size: 1.1rem;
    }
    .bg-gold-light { background-color: #FFF3E0; }
    .icon-feature {
      font-size: 3.8rem;
      color: var(--gold);
      margin-bottom: 1.2rem;
    }
    .whatsapp-float {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: #25D366;
      color: white;
      border-radius: 60px;
      padding: 20px 32px;
      font-size: 2.2rem;
      box-shadow: 0 8px 35px rgba(37,211,102,0.6);
      z-index: 999;
      transition: 0.3s;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 14px;
      border: 2px solid rgba(255,255,255,0.3);
    }
    .whatsapp-float:hover {
      transform: scale(1.1) translateY(-5px);
      background: #1da851;
      color: white;
      box-shadow: 0 15px 50px rgba(37,211,102,0.8);
    }
    .whatsapp-float span {
      font-size: 1.2rem;
      font-weight: 800;
    }
    footer {
      background: var(--dark);
      color: #ccc;
      padding: 2.5rem 0;
      text-align: center;
    }
    footer a { color: var(--gold); text-decoration: none; transition: 0.3s; }
    footer a:hover { color: white; }
    .promo-card {
      background: linear-gradient(135deg, var(--primary), #B33A1F);
      border-radius: 24px;
      padding: 2.5rem;
      color: white;
      box-shadow: 0 8px 30px rgba(216,74,42,0.4);
    }
    .promo-card h3 { color: var(--gold); }
    .social-icons a {
      display: inline-block;
      width: 55px;
      height: 55px;
      line-height: 55px;
      text-align: center;
      border-radius: 50%;
      background: rgba(255,255,255,0.1);
      color: white;
      font-size: 1.6rem;
      transition: 0.3s;
      margin: 0 8px;
    }
    .social-icons a:hover {
      background: var(--gold);
      color: var(--dark);
      transform: translateY(-5px);
    }
    .combo-badge {
      background: var(--gold);
      color: var(--dark);
      padding: 4px 14px;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 800;
    }
    .categoria-titulo {
      color: var(--primary);
      margin-bottom: 1.5rem;
      font-weight: 800;
    }
    .evento-card {
      background: white;
      border-radius: 24px;
      padding: 2rem;
      box-shadow: 0 8px 30px rgba(0,0,0,0.08);
      transition: 0.3s;
      height: 100%;
      text-align: center;
    }
    .evento-card:hover { transform: translateY(-8px); box-shadow: 0 15px 45px rgba(0,0,0,0.12); }
    .evento-card i { font-size: 3.5rem; color: var(--gold); margin-bottom: 1rem; }
    .testimonio-card {
      background: white;
      border-radius: 24px;
      padding: 2rem;
      box-shadow: 0 6px 20px rgba(0,0,0,0.06);
      border-left: 6px solid var(--gold);
    }
    .testimonio-card .nombre { font-weight: 700; color: var(--primary); }
    @media (max-width: 768px) {
      .hero h1 { font-size: 2.8rem; }
      .hero p { font-size: 1.2rem; }
      .whatsapp-float { padding: 14px 20px; font-size: 1.8rem; bottom: 20px; right: 20px; }
      .whatsapp-float span { display: none; }
      .section-title { font-size: 2.2rem; }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
    <div class="container">
      <a class="navbar-brand" href="#"><i class="fas fa-fire"></i> El Fogón <span>de la Huancaina</span></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto align-items-lg-center">
          <li class="nav-item"><a class="nav-link" href="#menu">Carta</a></li>
          <li class="nav-item"><a class="nav-link" href="#eventos">Eventos</a></li>
          <li class="nav-item"><a class="nav-link" href="#caja-china">Caja China</a></li>
          <li class="nav-item"><a class="nav-link" href="#contacto">Contacto</a></li>
          <li class="nav-item">
            <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20hacer%20un%20pedido" target="_blank" class="btn btn-primary-custom ms-2">
              <i class="fab fa-whatsapp"></i> Pedir
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <section id="inicio" class="hero">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-9">
          <h1 class="display-3 fw-bold">El Fogón de la Huancaina</h1>
          <p class="lead">¡El sabor de la sierra en tu mesa! <br> Desayunos, menús, caldos y eventos</p>
          <p><i class="fas fa-map-pin text-warning"></i> Av. Militar 1500, Lince – Puesto 35-36</p>
          <div class="d-flex flex-wrap justify-content-center gap-3 mt-4">
            <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20hacer%20un%20pedido" target="_blank" class="btn btn-whatsapp-lg">
              <i class="fab fa-whatsapp"></i> ¡Pide Ahora!
            </a>
            <a href="https://www.facebook.com/profile.php?id=61591147352866" target="_blank" class="btn btn-facebook btn-lg">
              <i class="fab fa-facebook"></i> Síguenos
            </a>
            <a href="#eventos" class="btn btn-gold btn-lg">
              <i class="fas fa-calendar-check"></i> Eventos
            </a>
          </div>
          <div class="mt-4">
            <span class="badge-day"><i class="fas fa-clock"></i> Lun-Vie 6am-3pm | Sáb-Dom 7am-2pm</span>
          </div>
          <div class="mt-3">
            <span class="badge bg-danger fs-6 p-3"><i class="fas fa-phone-alt"></i> ¡Llámanos! 942 789 973</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CARTA / MENÚ COMPLETO -->
  <section id="menu" class="py-5">
    <div class="container">
      <h2 class="section-title text-center">Nuestra Carta</h2>
      <p class="text-center text-muted mb-5">Desayunos desde S/. 2 y Menú completo S/. 13</p>

      <!-- DESAYUNOS -->
      <div class="mb-5">
        <h3 class="text-center categoria-titulo"><i class="fas fa-coffee"></i> Desayunos (Lun a Vie) – S/. 2 c/u</h3>
        <div class="row g-4">
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Quaker</h5><p class="desc">Avena caliente con leche, canela y frutas.</p><span class="precio">S/. 2</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-bread-slice"></i></div><h5>Pan con Queso</h5><p class="desc">Pan fresco con queso andino derretido.</p><span class="precio">S/. 2</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-egg"></i></div><h5>Pan con Huevo</h5><p class="desc">Pan tostado con huevo frito y salsa criolla.</p><span class="precio">S/. 2</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-leaf"></i></div><h5>Tortilla de Verduras</h5><p class="desc">Tortilla esponjosa con verduras frescas.</p><span class="precio">S/. 2</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-seedling"></i></div><h5>Choclo con Papa</h5><p class="desc">Choclo andino con papa sancochada y queso.</p><span class="precio">S/. 2</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-seedling"></i></div><h5>Papa con Huevo</h5><p class="desc">Papa sancochada con huevo y salsas.</p><span class="precio">S/. 2</span></div></div>
        </div>
      </div>

      <!-- PLATOS DEL DÍA (MENÚ COMPLETO) -->
      <div>
        <h3 class="text-center categoria-titulo"><i class="fas fa-utensil-spoon"></i> Platos del Día (Lun a Vie) – Menú completo S/. 13</h3>
        <p class="text-center text-muted">(Sopa + Segundo + Refresco)</p>
        <div class="row g-4">
          <!-- SOPAS -->
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-fish"></i></div><h5>Sopa de Choro</h5><p class="desc">Sopa cremosa con choros frescos.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-fish"></i></div><h5>Chupe de Pescado</h5><p class="desc">Chupe espeso con pescado, papas y huevo.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-drumstick-bite"></i></div><h5>Caldo de Gallina</h5><p class="desc">Caldo reconfortante con gallina y verduras.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-bowl-food"></i></div><h5>Menestrón</h5><p class="desc">Sopa de menestras con fideos y vegetales.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-bowl-food"></i></div><h5>Aguadito</h5><p class="desc">Sopa ligera de pollo con arroz y cilantro.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-bowl-food"></i></div><h5>Sopa de Pallares</h5><p class="desc">Sopa de pallares con costilla y hierbas.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <!-- SEGUNDOS -->
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-drumstick-bite"></i></div><h5>Adobo de Chancho</h5><p class="desc">Chancho adobado con especias y chicha.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-drumstick-bite"></i></div><h5>Adobo de Pollo</h5><p class="desc">Pollo adobado con especias y chicha.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-drumstick-bite"></i></div><h5>Arroz con Pollo</h5><p class="desc">Clásico arroz con pollo y salsa verde.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Locro de Zapallo</h5><p class="desc">Zapallo con filete de pollo y papas.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Picante de Carne</h5><p class="desc">Carne en salsa picante con papas.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Estofado</h5><p class="desc">Carne estofada con verduras y arroz.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Monguito Italiano</h5><p class="desc">Menestra de pallares con aderezo italiano.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Cau Cau</h5><p class="desc">Mondongo con papas y hierbabuena.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Pachamanca</h5><p class="desc">Carnes y papas cocidas a la piedra.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-fish"></i></div><h5>Trucha Frita</h5><p class="desc">Trucha fresca frita con ensalada.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-drumstick-bite"></i></div><h5>Cuy Frito</h5><p class="desc">Cuy crocante con papas y salsas.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Arroz con Pato</h5><p class="desc">Arroz con pato y culantro, plato bandera.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Caigua Rellena</h5><p class="desc">Caigua rellena de carne y verduras.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
          <div class="col-md-4 col-sm-6"><div class="menu-card text-center"><div class="icon"><i class="fas fa-utensils"></i></div><h5>Papa Rellena</h5><p class="desc">Papa rellena de carne y huevo, frita.</p><span class="precio">S/. 13</span><span class="combo-badge ms-2">+ Refresco</span></div></div>
        </div>
      </div>

      <div class="text-center mt-5">
        <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20hacer%20un%20pedido" target="_blank" class="btn btn-whatsapp-lg">
          <i class="fab fa-whatsapp"></i> ¡Pide tu menú completo!
        </a>
      </div>
    </div>
  </section>

  <!-- ESPECIALES DE FIN DE SEMANA -->
  <section id="especiales" class="py-5 bg-gold-light">
    <div class="container">
      <h2 class="section-title text-center">Especiales de Fin de Semana</h2>
      <p class="text-center text-muted mb-5">Sábados y Domingos – Caldos desde S/. 13 hasta S/. 17</p>
      <div class="row g-4 justify-content-center">
        <div class="col-md-4 col-sm-6">
          <div class="menu-card text-center">
            <div class="icon"><i class="fas fa-drumstick-bite"></i></div>
            <h5>Caldo de Gallina</h5>
            <p class="desc">Gallina criolla, fideos, huevo y hierbas.</p>
            <span class="precio">S/. 13</span>
          </div>
        </div>
        <div class="col-md-4 col-sm-6">
          <div class="menu-card text-center">
            <div class="icon"><i class="fas fa-drumstick-bite"></i></div>
            <h5>Caldo de Cordero</h5>
            <p class="desc">Cordero tierno con papas y menta.</p>
            <span class="precio">S/. 15</span>
          </div>
        </div>
        <div class="col-md-4 col-sm-6">
          <div class="menu-card text-center">
            <div class="icon"><i class="fas fa-seedling"></i></div>
            <h5>Caldo de Mote</h5>
            <p class="desc">Mote con hueso y verduras.</p>
            <span class="precio">S/. 17</span>
          </div>
        </div>
      </div>
      <div class="text-center mt-4">
        <span class="badge-day"><i class="fas fa-calendar-alt"></i> Sábado y Domingo – Pregunta por la Huancaina</span>
      </div>
      <div class="text-center mt-3">
        <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20reservar%20un%20caldo" target="_blank" class="btn btn-whatsapp-lg">
          <i class="fab fa-whatsapp"></i> Reserva tu caldo
        </a>
      </div>
    </div>
  </section>

  <!-- EVENTOS -->
  <section id="eventos" class="py-5">
    <div class="container">
      <h2 class="section-title text-center">Eventos Especiales</h2>
      <p class="text-center text-muted mb-5">Celebra con nosotros y sorprende a tus invitados con nuestro sazón</p>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="evento-card">
            <i class="fas fa-father"></i>
            <h4>Día del Padre</h4>
            <p>Menú especial para papá: chancho a la caja china, caldos y postres. ¡Reserva con anticipación!</p>
            <a href="https://wa.me/51942789973?text=Quiero%20reservar%20para%20el%20Día%20del%20Padre" target="_blank" class="btn btn-primary-custom btn-sm">Cotizar</a>
          </div>
        </div>
        <div class="col-md-4">
          <div class="evento-card">
            <i class="fas fa-birthday-cake"></i>
            <h4>Cumpleaños</h4>
            <p>Celebra con nosotros. Menús personalizados, tortas y decoración sencilla. ¡Pregunta por nuestros paquetes!</p>
            <a href="https://wa.me/51942789973?text=Quiero%20reservar%20para%20un%20cumpleaños" target="_blank" class="btn btn-primary-custom btn-sm">Cotizar</a>
          </div>
        </div>
        <div class="col-md-4">
          <div class="evento-card">
            <i class="fas fa-users"></i>
            <h4>Reuniones y más</h4>
            <p>Eventos empresariales, aniversarios, bautizos. Contamos con servicio de buffet y atención personalizada.</p>
            <a href="https://wa.me/51942789973?text=Quiero%20cotizar%20un%20evento" target="_blank" class="btn btn-primary-custom btn-sm">Cotizar</a>
          </div>
        </div>
      </div>
      <div class="text-center mt-4">
        <a href="https://wa.me/51942789973?text=Hola%20quiero%20información%20sobre%20eventos" target="_blank" class="btn btn-gold btn-lg">
          <i class="fab fa-whatsapp"></i> ¡Cotiza tu evento ahora!
        </a>
      </div>
    </div>
  </section>

  <!-- CHANCHO A LA CAJA CHINA -->
  <section id="caja-china" class="py-5 bg-gold-light">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <h2 class="section-title text-start" style="display:inline-block;">Chancho a la Caja China</h2>
          <p class="fs-5">El plato estrella para tus eventos. <strong>¡Crujiente por fuera, jugoso por dentro!</strong></p>
          <ul class="list-unstyled fs-6">
            <li><i class="fas fa-check-circle text-success"></i> Ideal para cumpleaños, reuniones y celebraciones</li>
            <li><i class="fas fa-check-circle text-success"></i> Servimos a domicilio en toda Lima</li>
            <li><i class="fas fa-check-circle text-success"></i> Precio desde S/. 120 (para 10 personas)</li>
            <li><i class="fas fa-check-circle text-success"></i> Incluye guarniciones: papas, camote, salsas</li>
          </ul>
          <div class="mt-3">
            <a href="https://wa.me/51942789973?text=Quiero%20pedir%20chancho%20a%20la%20caja%20china" target="_blank" class="btn btn-whatsapp-lg">
              <i class="fab fa-whatsapp"></i> ¡Pide tu Chancho!
            </a>
          </div>
        </div>
        <div class="col-lg-6 text-center">
          <div style="background: var(--gold); border-radius: 30px; padding: 2rem; color: var(--dark);">
            <i class="fas fa-piggy-bank" style="font-size: 8rem; color: var(--primary);"></i>
            <h3 class="mt-3">¡El mejor chancho de Lince!</h3>
            <p>Preparado con receta secreta de la abuela. ¡No te lo pierdas!</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIOS -->
  <section class="py-5">
    <div class="container">
      <h2 class="section-title text-center">Lo que dicen nuestros clientes</h2>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="testimonio-card">
            <p><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i></p>
            <p>"El mejor caldo de gallina que he probado en Lima. Mi papá quedó encantado."</p>
            <p class="nombre">– Carlos R.</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="testimonio-card">
            <p><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i></p>
            <p>"Pedimos el chancho a la caja china para el cumpleaños de mi hijo y fue un éxito. ¡Todos pidieron repetir!"</p>
            <p class="nombre">– María G.</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="testimonio-card">
            <p><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i><i class="fas fa-star text-warning"></i></p>
            <p>"Los desayunos son súper económicos y deliciosos. Voy todas las mañanas."</p>
            <p class="nombre">– Laura M.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACTO -->
  <section id="contacto" class="py-5 bg-gold-light">
    <div class="container">
      <h2 class="section-title text-center">¡Contáctanos ya!</h2>
      <div class="row g-4 mt-3">
        <div class="col-lg-6">
          <div class="bg-white p-4 rounded-4 shadow-sm h-100">
            <h4><i class="fas fa-store"></i> El Fogón de la Huancaina</h4>
            <p><i class="fas fa-map-pin text-danger"></i> Av. Militar 1500, Lince – Mercado 10 de Junio, Puesto 35-36</p>
            <p><i class="fas fa-phone-alt text-success"></i> <strong>942 789 973</strong> (llama o escribe)</p>
            <p><i class="fas fa-clock text-warning"></i> Horario:</p>
            <ul class="list-unstyled">
              <li><strong>Lunes a Viernes:</strong> 6:00 am – 3:00 pm</li>
              <li><strong>Sábados y Domingos:</strong> 7:00 am – 2:00 pm</li>
            </ul>
            <div class="d-flex flex-wrap gap-3 mt-4">
              <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20hacer%20un%20pedido" target="_blank" class="btn btn-success btn-lg flex-fill"><i class="fab fa-whatsapp"></i> WhatsApp</a>
              <a href="https://www.facebook.com/profile.php?id=61591147352866" target="_blank" class="btn btn-facebook btn-lg flex-fill"><i class="fab fa-facebook"></i> Facebook</a>
            </div>
            <div class="mt-3">
              <a href="tel:+51942789973" class="btn btn-primary-custom btn-lg w-100"><i class="fas fa-phone"></i> ¡Llámanos!</a>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="bg-white p-4 rounded-4 shadow-sm h-100">
            <h4><i class="fas fa-map"></i> Ubicación</h4>
            <div class="ratio ratio-16x9">
              <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3901.1422455309353!2d-77.03776118517514!3d-12.082536845676672!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMTLCsDA0JzU3LjEiUyA3N8KwMDInMDYuMSJX!5e0!3m2!1ses!2spe!4v1647535549325!5m2!1ses!2spe" allowfullscreen="" loading="lazy"></iframe>
            </div>
            <p class="mt-2 text-muted small">Av. Militar 1500, Lince (Mercado 10 de Junio)</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p class="mb-1">&copy; 2025 <strong>El Fogón de la Huancaina</strong> – Sabor que une a la familia</p>
      <p class="small">Puesto 35-36, Mercado 10 de Junio – Av. Militar 1500, Lince</p>
      <div class="social-icons">
        <a href="https://wa.me/51942789973" target="_blank"><i class="fab fa-whatsapp"></i></a>
        <a href="tel:+51942789973"><i class="fas fa-phone"></i></a>
        <a href="https://www.facebook.com/profile.php?id=61591147352866" target="_blank"><i class="fab fa-facebook"></i></a>
        <a href="#"><i class="fas fa-envelope"></i></a>
      </div>
      <p class="mt-2"><a href="https://wa.me/51942789973?text=Quiero%20recibir%20ofertas" target="_blank" class="btn btn-gold btn-sm">Suscríbete a ofertas</a></p>
    </div>
  </footer>

  <!-- Botón flotante WhatsApp -->
  <a href="https://wa.me/51942789973?text=Hola%20El%20Fogón%20de%20la%20Huancaina%2C%20quisiera%20hacer%20un%20pedido" target="_blank" class="whatsapp-float">
    <i class="fab fa-whatsapp"></i> <span>¡Escríbenos!</span>
  </a>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Smooth scroll
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });
  </script>
</body>
</html>
