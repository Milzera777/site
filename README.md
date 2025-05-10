<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Assistência Técnica Especializada</title>
  <link rel="icon" href="https://cdn-icons-png.flaticon.com/512/2920/2920265.png" type="image/png">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"/>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f8f9fa;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }

    header {
      background-color: #002b5c;
      color: white;
      padding: 60px 20px;
      text-align: center;
      animation: fadeIn 1s ease-in-out;
    }

    header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.2rem;
    }

    .toggle-btn {
      background: #0072ce;
      color: white;
      padding: 12px 24px;
      border: none;
      border-radius: 4px;
      font-weight: bold;
      margin-top: 20px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }

    .toggle-btn:hover {
      background: #005fa3;
      transform: translateY(-2px);
    }

    nav {
      background-color: #f1f1f1;
      padding: 15px 20px;
      display: flex;
      justify-content: center;
      gap: 20px;
      border-bottom: 1px solid #ddd;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav a {
      color: #002b5c;
      text-decoration: none;
      font-weight: 600;
      padding: 8px 12px;
      transition: color 0.3s ease, transform 0.3s;
    }

    nav a:hover {
      color: #0072ce;
      transform: translateY(-2px);
    }

    section {
      max-width: 1100px;
      margin: 60px auto;
      padding: 0 20px;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.6s ease-out, transform 0.6s ease-out;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      font-size: 2rem;
      color: #002b5c;
      margin-bottom: 20px;
      border-bottom: 3px solid #0072ce;
      display: inline-block;
      padding-bottom: 5px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      background: white;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 6px;
      text-align: center;
      transition: box-shadow 0.3s, transform 0.3s;
      opacity: 0;
      transform: translateY(20px);
    }

    .card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .card:hover {
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      border-radius: 6px;
      margin-bottom: 15px;
    }

    .gif-container {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
      margin-top: 30px;
    }

    .gif-container img {
      width: 100%;
      max-width: 280px;
      border-radius: 6px;
      opacity: 0;
      transform: scale(0.9);
      transition: all 0.6s ease-out;
    }

    .gif-container img.visible {
      opacity: 1;
      transform: scale(1);
    }

    ul {
      margin-left: 20px;
      list-style: disc;
      line-height: 1.8;
    }

    footer {
      background-color: #002b5c;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      margin-top: 40px;
    }

    .whatsapp-float {
      position: fixed;
      width: 60px;
      height: 60px;
      bottom: 25px;
      right: 25px;
      z-index: 1000;
      background-color: #25d366;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: transform 0.3s;
    }

    .whatsapp-float:hover {
      transform: scale(1.1);
    }

    .whatsapp-float img {
      width: 35px;
      height: 35px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Media Queries Responsivas */
    @media (max-width: 768px) {
      header {
        padding: 40px 15px;
      }

      header h1 {
        font-size: 2rem;
      }

      header p {
        font-size: 1rem;
      }

      .toggle-btn {
        padding: 10px 20px;
        font-size: 0.95rem;
      }

      nav {
        flex-direction: column;
        gap: 10px;
        padding: 10px 15px;
      }

      nav a {
        font-size: 1rem;
      }

      section {
        margin: 40px auto;
        padding: 0 15px;
      }

      h2 {
        font-size: 1.6rem;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .card img {
        height: auto;
      }

      .gif-container {
        flex-direction: column;
        align-items: center;
      }

      .gif-container img {
        max-width: 100%;
      }

      .whatsapp-float {
        width: 50px;
        height: 50px;
        bottom: 15px;
        right: 15px;
      }

      .whatsapp-float img {
        width: 28px;
        height: 28px;
      }

      footer {
        font-size: 0.8rem;
        padding: 15px;
      }
    }

    @media (max-width: 480px) {
      header h1 {
        font-size: 1.5rem;
      }

      h2 {
        font-size: 1.4rem;
      }

      .toggle-btn {
        width: 100%;
        font-size: 1rem;
      }

      nav a {
        padding: 10px;
        font-size: 1rem;
        width: 100%;
        text-align: center;
      }

      .cards {
        gap: 15px;
      }

      section p, ul li {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1><i class="fas fa-tools"></i> BCJ Impressoras</h1>
    <p>Especialistas em conserto e manutenção de impressoras e computadores</p>
    <button class="toggle-btn" onclick="document.getElementById('sobre').scrollIntoView({ behavior: 'smooth' })">Iniciar</button>
  </header>

  <nav>
    <a href="#sobre">Sobre</a>
    <a href="#servicos">Serviços</a>
    <a href="#contato">Contato</a>
  </nav>

  <section id="sobre">
    <h2>Sobre Nós</h2>
    <p>Com mais de uma década de experiência, somos especialistas em oferecer soluções ágeis e eficientes para impressoras, computadores e manutenção técnica.</p>

    <div class="cards">
      <div class="card">
        <img src="https://www.contabilista.com.br/media/wysiwyg/impressoras/img1.png" alt="Impressora">
        <p>Impressoras modernas e multifuncionais</p>
      </div>
      <div class="card">
        <img src="https://infrainfo.com.br/wp-content/uploads/2018/03/computadores-img-300x176.png" alt="Manutenção de PC">
        <p>Manutenção de computadores e notebooks</p>
      </div>
      <div class="card">
        <img src="https://www.updateti.com.br/wp-content/uploads/2023/06/venda-de-suprimentos-e1687295958621.webp" alt="Peças técnicas">
        <p>Peças técnicas e substituições eficientes</p>
      </div>
    </div>
  </section>

  <section id="servicos">
    <h2>Nossos Serviços</h2>
    <ul>
      <li>Manutenção preventiva e corretiva</li>
      <li>Reparo de impressoras jato de tinta e laser</li>
      <li>Substituição de peças</li>
      <li>Atendimento em domicílio para empresas</li>
    </ul>
    <div class="gif-container">
      <img src="https://preservetoner.com.br/wp-content/uploads/2020/07/impressoras1.png" alt="Reparo impressora">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTLRS-anzqjptzRMlBFYaVuCuvMDrjcG_OkeQ&s" alt="Manutenção de PC">
      <img src="https://www.prepara.com.br/media/magefan_blog/tmp/capa-tecnico-de-informatica.jpg" alt="Técnico trabalhando">
    </div>
  </section>

  <section id="contato">
    <h2>Contato</h2>
    <p><i class="fas fa-envelope"></i> Email: ballyhoocopiadoras@gmail.com </p>
    <p><i class="fas fa-phone-alt"></i> Telefone: (11) 5068-1370</p>
    <p><i class="fas fa-map-marker-alt"></i> Endereço: Rua Sussurana 103, Ipiranga, São Paulo - 04281070</p>
  </section>

  <footer>
    <p>&copy; 2025 - Todos os direitos reservados | Alunos UNINOVE.</p>
  </footer>

  <a href="https://api.whatsapp.com/send/?phone=5511944557246&text&type=phone_number&app_absent=0" class="whatsapp-float" target="_blank">
    <img src="https://cdn-icons-png.flaticon.com/512/733/733585.png" alt="WhatsApp">
  </a>

  <script>
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, {
      threshold: 0.1
    });

    document.querySelectorAll('section, .card, .gif-container img').forEach(el => {
      observer.observe(el);
    });
  </script>
</body>
</html>
