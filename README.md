[index (1).html](https://github.com/user-attachments/files/22414359/index.1.html)
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Raioxtech — Trabalho Escolar</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@300;500;700&display=swap"
      rel="stylesheet"
    />
    <style>
      :root {
         --primary: #2465c5;
  --accent: #245399;
  --bg: #E0ECDE;
  --bg-light: #CDE0C9;
  --text: #2C2C2C;
  --muted: #395691;
  --radius: 14px;
  font-family: 'Inter', sans-serif;
      }

      * { margin: 0; padding: 0; box-sizing: border-box; }
      html { scroll-behavior: smooth; }
      body { background: var(--bg); color: var(--text); line-height: 1.6; transition: background 0.3s, color 0.3s; }

      /* NAVBAR */
      .navbar {
        background: white;
        border-bottom: 1px solid #d1d5db;
        position: sticky;
        top: 0;
        z-index: 10;
      }
      .navbar-container {
        max-width: 1000px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 14px 20px;
      }
      .logo {
        font-size: 1.5rem;
        font-weight: 700;
        color: var(--primary);
        letter-spacing: 1px;
      }
      .nav-links { display: flex; list-style: none; gap: 20px; }
      .nav-links a {
        color: var(--text);
        font-weight: 500;
        text-decoration: none;
        transition: color 0.2s;
      }
      .nav-links a:hover { color: var(--primary); }

      /* HERO */
      .hero {
        background: var(--bg-light);
        color: var(--text);
        padding: 50px 20px;
        text-align: center;
        border-bottom: 1px solid #d1d5db;
      }
      .hero h2 { font-size: 2rem; margin-bottom: 10px; }

      /* CONTENT */
      .container { max-width: 900px; margin: auto; padding: 20px; }
      .block {
        background: white;
        padding: 24px;
        margin: 20px 0;
        border-radius: var(--radius);
        box-shadow: 0 4px 10px rgba(0,0,0,0.08);
        transition: transform 0.2s ease, box-shadow 0.2s ease;
      }
      body.dark .block { background: #2a2b31; }
      .block:hover { transform: translateY(-3px); box-shadow: 0 8px 16px rgba(0,0,0,0.12); }
      .block.alt { background: var(--bg-light); }
      body.dark .block.alt { background: #20232a; }
      .block h2 { margin-bottom: 12px; font-size: 1.3rem; }

      /* AUTORES EM DUAS COLUNAS */
      #autoria { text-align: center; }
      .author-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
        margin-top: 20px;
        justify-items: center;
      }
      .author-card {
        background: #f8f8f8;
        padding: 15px;
        width: 100%;
        max-width: 280px;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
        text-align: center;
        transition: transform 0.2s ease, box-shadow 0.2s ease;
      }
      .author-card:hover { transform: translateY(-3px); box-shadow: 0 6px 14px rgba(0, 0, 0, 0.15); }
      .author-card h3 { margin-bottom: 8px; font-weight: bold; }
      .author-card p { font-size: 0.95rem; margin-bottom: 8px; }
      .author-card a {
        display: inline-block;
        margin-top: 5px;
        color: #0066cc;
        font-weight: 500;
        text-decoration: none;
      }
      .author-card a:hover { text-decoration: underline; }
      @media (max-width: 600px) {
        .author-grid { grid-template-columns: 1fr; }
      }

      /* VIDEO RESPONSIVO */
      .video-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 15px;
      }
      .video-wrapper iframe {
        max-width: 100%;
        border-radius: var(--radius);
        box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      }

      /* Botão voltar ao topo */
      #backToTop {
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: #222;
        color: white;
        border: none;
        padding: 10px 15px;
        border-radius: 50%;
        font-size: 18px;
        cursor: pointer;
        display: none;
        box-shadow: 0 4px 8px rgba(0,0,0,0.3);
      }
      #backToTop:hover { background: #444; }

      /* Curiosidades */
      .curiosidades-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 15px;
        margin-top: 15px;
      }
      .curiosidade-card {
        background: #f2f2f2;
        padding: 15px;
        border-radius: 12px;
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        text-align: center;
        font-size: 1rem;
        transition: transform 0.2s ease;
      }
      .curiosidade-card:hover { transform: scale(1.02); }
      .curiosidade-card p { margin: 10px 0 0; }

      .school-info {
        margin-top: 10px;
        font-size: 0.95rem;
        color: var(--muted);
      }
    </style>
  </head>
  <body>
    <!-- NAVBAR -->
    <nav class="navbar">
      <div class="navbar-container">
        <h1 class="logo">Chuva Ácida</h1>
        <ul class="nav-links">
          <li><a href="#definicao">Definição</a></li>
          <li><a href="#missão">missão</a></li>
          <li><a href="#valores">valores</a></li>
          <li><a href="#público alvo">público alvo</a></li>
          <li><a href="#curiosidades">Curiosidades</a></li>
          <li><a href="#video">Vídeo</a></li>
          <li><a href="#autoria">Autores</a></li>
        </ul>
      </div>
    </nav>

    <!-- HEADER -->
    <header class="hero">
      <div class="hero-content">
        <h2>Entenda sobre</h2>
        <p>Definição, missão, valores e público alvo</p>
      </div>
    </header>

    <main class="container">
      <section id="definicao" class="block">
        <h2>O que é a Raioxtech?</h2>
        <p>
         Câmera Instantânea de Triagem raioxtech é um conceito inovador pensado para ambientes como aeroportos e hospitais, 
         onde o tempo de resposta é Instantâneo. Ela funciona como uma câmera avançada de triagem não-invasiva,
         projetada para captar imagens internas em tempo real, oferecendo uma visão imediata que auxilia equipes de  
         segurança e saúde na tomada de decisões.
        </p>
      </section>

     

      <section id="Missão" class="block alt">
        <h2>Missão</h2>
        <ul>
          <li>A nossa missão é deixar a vida mais prática e segura <strong>trazendo uma câmera que ajuda</strong> 
            a enxergar por dentro de forma rápida e sem complicação.</li>
          <li>A ideia é apoiar hospitais <strong> e aeroportos para que possam </strong>cuidar melhor das pessoas e garantir mais</li>
          <li>tranquilidade no dia a dia</li>
        </ul>
      </section>

      <section id="Público alvo" class="block">
        <h2>Público alvo</h2>
        <ul>
          <li><strong>Aeroportos:</strong> agilizar a segurança e reduzir processos invasivos.</li>
          <li><strong>Hospitais/Clínicas:</strong> apoiar na triagem rápida de pacientes.</li>
          <li><strong>Eventos de grande porte:</strong>  garantir segurança em shows, estádios e feiras.</li>
          <li><strong>Bancos e áreas restritas: </strong> aumentar a proteção em ambientes de alto risco.</li>
          <li><strong>Grandes empresas:</strong> controlar a entrada e saída de objetos permitidos, reforçando a segurança interna.</li>
        </ul>
      </section>

      <section id="valores" class="block alt">
        <h2>valores</h2>
        <ul>
          <li>Privacidade:imagens usadas apenas para exames médicos ou controle de segurança, respeitando a intimidade das pessoas.</li>
          <li>Benefício social:priorizar a saúde dos pacientes e a segurança de todos no ambiente.</li>
          <li>Transparência: deixar claro como a câmera funciona e para que suas imagens são usadas.</li>
          <li>Segurança dos dados:proteger todas as imagens contra acesso não autorizado ou vazamentos.</li>
          
      <!-- CURIOSIDADES -->
      <section id="curiosidades" class="block">
        <h2>Curiosidades</h2>
        <div class="curiosidades-grid">
          <div class="curiosidade-card">
            🔋 <p>Bateria de longa duração – funciona horas seguidas sem precisar recarregar.</p>
          </div>
          <div class="curiosidade-card">
             📷 <p>Imagens instantâneas – captura e envia fotos em tempo real.</p>
          </div>
          <div class="curiosidade-card">
           ⚡<p>Alta precisão – identifica objetos ou áreas médicas com grande clareza.</p>
          </div>
        </div>
      </section>

     
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/9egpauSj0IA"
            title="foto ilustrativa do projeto"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </section>
    </main>

    <!-- AUTORES -->
    <section id="autoria" class="block">
      <h2>Autores do Trabalho</h2>
      <div class="author-grid">
        <div class="author-card">
          <h3>Cauã</h3>
          <p>Responsável pela pesquisa sobre <strong>Funcionalidades</strong>.</p>
    
        </div>
        <div class="author-card">
          <h3>Victor Kaique</h3>
          <p>Responsável pelo desenvolvimento de: <strong>Missão</strong>.</p>
          
        </div>
        <div class="author-card">
          <h3>Igor Carvalho</h3>
          <p>Responsável pela pesquisa sobre <strong>Público alvo</strong>.</p>
          
        </div>
        <div class="author-card">
          <h3>Henzel e thierry</h3>
          <p>Responsável pela pesquisa sobre <strong>valores e definição</strong>.</p>
        
        </div>
        <div class="author-card">
          <h3>Ariane</h3>
          <p>Organização, revisão e formatação do conteúdo.</p>
          
      </div>
      <p class="school-info"><strong>Instituição:</strong>Natasha </p>
      <p class="school-info"><strong>Empresas:</strong>Sky Chefs, Colégio Mater e Impala,</p>
    </section>

    <!-- BOTÃO VOLTAR AO TOPO -->
    <button id="backToTop" title="Voltar ao topo">⬆</button>

    <script>
      // Botão voltar ao topo
      const backToTopBtn = document.getElementById("backToTop");
      window.addEventListener("scroll", () => {
        backToTopBtn.style.display = window.scrollY > 300 ? "block" : "none";
      });
      backToTopBtn.addEventListener("click", () => {
        window.scrollTo({ top: 0, behavior: "smooth" });
      });
    </script>
  </body>
</html>
