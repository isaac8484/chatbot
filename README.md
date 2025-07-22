<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Chatbot com Botão Flutuante</title>

  <!-- Estilo do site -->
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #121212;
      color: white;
    }

    header {
      background-color: #2196f3;
      padding: 1rem;
      text-align: center;
    }

    main {
      padding: 2rem;
      text-align: center;
    }

    footer {
      background-color: #1c1c1c;
      padding: 1rem;
      text-align: center;
    }

    /* Container do chatbot (inicialmente escondido) */
    #mcontext {
      display: none;
      position: fixed;
      bottom: 100px;
      right: 20px;
      width: 360px;
      height: 600px;
      box-shadow: 0 0 15px rgba(0,0,0,0.5);
      z-index: 999;
      background-color: #000;
      border-radius: 10px;
      overflow: hidden;
    }

    /* Botão flutuante */
    #openChatBtn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #2196f3;
      color: white;
      border: none;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      font-size: 28px;
      cursor: pointer;
      z-index: 1000;
      box-shadow: 0 4px 10px rgba(0,0,0,0.4);
      transition: background-color 0.3s;
    }

    #openChatBtn:hover {
      background-color: #1976d2;
    }
  </style>
</head>
<body>

  <header>
    <h1>Bem-vindo ao Chatbot</h1>
  </header>

  <main>
    <p>Clique no escudo para conversar com nosso assistente virtual.</p>
  </main>

  <footer>
    &copy; 2025 - SeuNome ou Empresa
  </footer>

  <!-- Botão flutuante com símbolo de escudo 🛡️ -->
  <button id="openChatBtn">🛡️</button>

  <!-- Chatbot oculto inicialmente -->
  <div id="mcontext"></div>

  <!-- Script do chatbot -->
  <script
    mode="embed"
    isolate="true"
    themecolor="#2196f3"
    header="off"
    accentcolor="#000000"
    textcolor="white"
    id="webchat"
    src="https://cdn.machaao.com/prod/web/js/embed.js"
    type="text/javascript"
    mkey="ZWNmNjU5ZjAtNjM0MC0xMWYwLWI0NmEtOTNmMmFkMWRkNDYw"
    style="min-height: 480px">
  </script>

  <!-- Script para abrir/fechar o chat -->
  <script>
    const btn = document.getElementById('openChatBtn');
    const chat = document.getElementById('mcontext');
    let isOpen = false;

    btn.addEventListener('click', () => {
      isOpen = !isOpen;
      chat.style.display = isOpen ? 'block' : 'none';
    });
  </script>

</body>
</html>
