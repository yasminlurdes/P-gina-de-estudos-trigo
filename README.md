Aqui está o código HTML completo e estilizado com CSS em um único arquivo. Ele cria uma página de estudos moderna, responsiva e estruturada para um estudante vestibulando revisar a **Genética do Trigo**.

Para visualizar, basta salvar o código abaixo em um arquivo chamado `index.html` e abri-lo em qualquer navegador.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hub de Estudos - Genética do Trigo</title>
  <style>
    :root {
      --bg-color: #f4f6f9;
      --card-bg: #ffffff;
      --primary: #2563eb;
      --primary-hover: #1d4ed8;
      --text-main: #1e293b;
      --text-muted: #64748b;
      --border-color: #e2e8f0;
      --accent-pdf: #ef4444;
      --accent-video: #dc2626;
      --accent-photo: #059669;
      --accent-note: #d97706;
      --accent-quiz: #7c3aed;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-main);
      padding-bottom: 40px;
    }

    header {
      background-color: var(--card-bg);
      border-bottom: 1px solid var(--border-color);
      padding: 16px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .nav-back {
      text-decoration: none;
      color: var(--primary);
      font-weight: 600;
    }

    header h1 {
      font-size: 1.1rem;
      color: var(--text-main);
    }

    .container {
      max-width: 800px;
      margin: 24px auto;
      padding: 0 16px;
    }

    .banner {
      background: linear-gradient(135deg, #1e3a8a, #3b82f6);
      color: white;
      padding: 24px;
      border-radius: 12px;
      margin-bottom: 24px;
    }

    .banner .subject {
      text-transform: uppercase;
      font-size: 0.8rem;
      letter-spacing: 1px;
      opacity: 0.8;
      font-weight: 700;
    }

    .banner h2 {
      margin: 8px 0 16px 0;
      font-size: 1.5rem;
    }

    .progress-bar-bg {
      background: rgba(255, 255, 255, 0.2);
      height: 8px;
      border-radius: 4px;
      overflow: hidden;
      margin-bottom: 8px;
    }

    .progress-bar-fill {
      background: #10b981;
      height: 100%;
      width: 55%;
    }

    .progress-text {
      font-size: 0.85rem;
      opacity: 0.9;
    }

    .filters {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      padding-bottom: 8px;
      margin-bottom: 24px;
    }

    .filter-btn {
      background: var(--card-bg);
      border: 1px solid var(--border-color);
      padding: 8px 16px;
      border-radius: 20px;
      font-size: 0.875rem;
      cursor: pointer;
      white-space: nowrap;
      color: var(--text-muted);
      font-weight: 500;
    }

    .filter-btn.active {
      background: var(--primary);
      color: white;
      border-color: var(--primary);
    }

    .materials-grid {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    }

    .card-header {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 0.8rem;
      font-weight: 700;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .tag-pdf { color: var(--accent-pdf); }
    .tag-video { color: var(--accent-video); }
    .tag-photo { color: var(--accent-photo); }
    .tag-note { color: var(--accent-note); }
    .tag-quiz { color: var(--accent-quiz); }

    .card h3 {
      font-size: 1.1rem;
      margin-bottom: 8px;
    }

    .card p, .card ul {
      color: var(--text-muted);
      font-size: 0.925rem;
      line-height: 1.5;
      margin-bottom: 16px;
    }

    .card ul {
      padding-left: 20px;
    }

    .card-meta {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 12px;
    }

    .btn {
      display: inline-block;
      padding: 8px 16px;
      border-radius: 6px;
      text-decoration: none;
      font-size: 0.875rem;
      font-weight: 600;
      cursor: pointer;
      border: none;
    }

    .btn-primary {
      background: var(--primary);
      color: white;
    }

    .btn-primary:hover {
      background: var(--primary-hover);
    }

    .btn-outline {
      background: transparent;
      border: 1px solid var(--border-color);
      color: var(--text-main);
    }

    .actions-footer {
      margin-top: 32px;
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .actions-footer .btn {
      flex: 1;
      text-align: center;
      padding: 12px;
    }

    @media (max-width: 600px) {
      .actions-footer {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>

  <header>
    <a href="#" class="nav-back">← Voltar</a>
    <h1>Hub de Estudos</h1>
    <span style="cursor:pointer;">🔍</span>
  </header>

  <div class="container">
    
    <!-- BANNER DE PROGRESSO -->
    <section class="banner">
      <div class="subject">Biologia • Genética</div>
      <h2>Genética do Trigo: Poliploidia e Herança Quantitativa</h2>
      <div class="progress-bar-bg">
        <div class="progress-bar-fill"></div>
      </div>
      <div class="progress-text">55% do tema concluído • 5 materiais salvos</div>
    </section>

    <!-- FILTROS -->
    <nav class="filters">
      <button class="filter-btn active">Todos (5)</button>
      <button class="filter-btn">PDFs</button>
      <button class="filter-btn">Vídeos</button>
      <button class="filter-btn">Lousa</button>
      <button class="filter-btn">Notas</button>
      <button class="filter-btn">Questões</button>
    </nav>

    <!-- LISTA DE CONTEÚDOS -->
    <main class="materials-grid">

      <!-- PDF CARD -->
      <article class="card">
        <div class="card-header tag-pdf">📄 PDF de Aula</div>
        <h3>Apostila: Genética e Origem do Trigo Hexaploide</h3>
        <p>Estudo detalhado sobre a evolução do trigo moderno (<em>Triticum aestivum</em>) via hibridização de três espécies ancestrais (genomas AABBDD).</p>
        <div class="card-meta">14 páginas • PDF (3.8 MB)</div>
        <a href="#" class="btn btn-primary">Abrir PDF</a>
      </article>

      <!-- VIDEO CARD -->
      <article class="card">
        <div class="card-header tag-video">🎥 Videoaula</div>
        <h3>Herança Poligênica e a Cor dos Grãos de Trigo</h3>
        <p>Explicação do experimento histórico de Nilsson-Ehle. Entenda a distribuição em curva normal e a variação fenotípica do vermelho-escuro ao branco.</p>
        <div class="card-meta">Canal Biologia Gabarito • Duração: 16 min</div>
        <a href="#" class="btn btn-primary">Assistir Vídeo</a>
      </article>

      <!-- FOTO CARD -->
      <article class="card">
        <div class="card-header tag-photo">📸 Foto da Lousa</div>
        <h3>Quadro Resumo: Diagrama de Punnett e Alelos Aditivos</h3>
        <p>Foto do quadro com a fórmula do número de classes fenotípicas (2n + 1) e exemplo de cruzamento de tri-híbridos (AaBbCc × AaBbCc).</p>
        <div class="card-meta">Capturado da aula de Quarta-feira</div>
        <a href="#" class="btn btn-outline">Visualizar Imagem</a>
      </article>

      <!-- LEMBRETES CARD -->
      <article class="card">
        <div class="card-header tag-note">📝 Anotação & Lembretes da Prova</div>
        <h3>Bizus para o ENEM / Vestibulares</h3>
        <ul>
          <li><strong>Poliploidia:</strong> O trigo comercial é alohexaploide (2n = 6x = 42 cromossomos).</li>
          <li><strong>Herança Quantitativa:</strong> Alelos maiúsculos (A, B, C) somam pigmento ao grão (efeito aditivo).</li>
          <li><strong>Atenção:</strong> Não confundir herança quantitativa com polialelia (alelos múltiplos)!</li>
        </ul>
        <div class="card-meta">Atualizado há 2 dias</div>
        <a href="#" class="btn btn-outline">Editar Anotação</a>
      </article>

      <!-- QUESTÕES CARD -->
      <article class="card">
        <div class="card-header tag-quiz">🧠 Exercícios de Fixação</div>
        <h3>Simulado Rápidos: 5 Questões do Tema</h3>
        <p><strong>Exemplo de questão:</strong> No cruzamento de tri-híbridos (AaBbCc × AaBbCc), qual a probabilidade de obter uma planta com grãos vermelho-escuro (AABBCC)?</p>
        <div class="card-meta">Gabarito comentado incluído • Nível Médio</div>
        <a href="#" class="btn btn-primary">Iniciar Questões</a>
      </article>

    </main>

    <!-- AÇÕES DE RODAPÉ -->
    <div class="actions-footer">
      <button class="btn btn-outline">+ Adicionar Novo Material</button>
      <button class="btn btn-primary">Refazer Simulado do Tema</button>
    </div>

  </div>

</body>
</html>

```
