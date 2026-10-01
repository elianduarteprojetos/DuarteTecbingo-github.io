<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bingo Pro - Multi Cartelas, PIX & Ciclo Automático | DuarteTec</title>
    
    <!-- Configurações para Aplicativo / PWA (Capa e Ícone) -->
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#4f46e5">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="Bingo Pro">
    <link rel="apple-touch-icon" href="icon-192.png">

    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root { 
            --bg: #f1f5f9; 
            --surface: #ffffff; 
            --primary: #4f46e5; 
            --primary-hover: #4338ca;
            --text-main: #0f172a;
            --text-muted: #64748b;
            --danger: #ef4444; 
            --success: #10b981; 
            --warning: #f59e0b;
            --border: #e2e8f0;
            --globo-bg: #1e293b;
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.1);
            --shadow-md: 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
            --shadow-lg: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
            --radius: 12px;
        }

        * { box-sizing: border-box; }
        
        body { 
            font-family: 'Outfit', sans-serif; 
            background: var(--bg); 
            color: var(--text-main); 
            margin: 0; 
            padding: 20px; 
            display: flex; 
            flex-direction: column; 
            align-items: center;
            min-height: 100vh;
        }

        .container { max-width: 1200px; width: 100%; display: flex; flex-direction: column; gap: 24px; transition: all 0.3s ease; flex: 1; }
        .container.expandida { max-width: 1600px; } 
        
        .card { 
            background: var(--surface); 
            padding: 30px; 
            border-radius: var(--radius); 
            box-shadow: var(--shadow-md); 
            border: 1px solid var(--border);
        }
        
        #tela-login, #tela-admin, #tela-jogador { display: none; animation: fadeIn 0.4s ease-out; }
        .active { display: block !important; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        h1, h2, h3, h4 { margin-top: 0; color: var(--text-main); font-weight: 800; letter-spacing: -0.02em; }
        p { color: var(--text-muted); line-height: 1.5; }
        
        input, select, button { 
            padding: 14px 20px; 
            border-radius: 8px; 
            font-size: 16px; 
            font-family: inherit;
            width: 100%; 
            margin-bottom: 12px; 
            transition: all 0.2s;
        }
        
        input, select { border: 2px solid var(--border); background: #f8fafc; color: var(--text-main); font-weight: 600; }
        input:focus, select:focus { outline: none; border-color: var(--primary); background: var(--surface); box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.2); }
        
        button { background: var(--primary); color: white; border: none; font-weight: 600; cursor: pointer; display: inline-flex; align-items: center; justify-content: center; gap: 8px; }
        button:hover { background: var(--primary-hover); transform: translateY(-1px); box-shadow: var(--shadow-md); }
        button:active { transform: translateY(0); }
        
        button.danger { background: var(--danger); }
        button.danger:hover { background: #dc2626; }
        button.success { background: var(--success); }
        button.success:hover { background: #059669; }
        button.warning { background: var(--warning); color: #78350f; }
        button.warning:hover { background: #d97706; color: white; }
        button.outline { background: transparent; border: 2px solid var(--border); color: var(--text-main); }
        button.outline:hover { border-color: var(--primary); color: var(--primary); background: #eef2ff; }

        .game-layout { display: grid; grid-template-columns: 1fr; gap: 24px; transition: all 0.3s ease; }
        @media(min-width: 900px) { .game-layout { grid-template-columns: 380px 1fr; } }

        .globo-area { text-align: center; padding: 30px 20px; background: var(--globo-bg); color: white; border-radius: var(--radius); margin-bottom: 24px; box-shadow: inset 0 2px 10px rgba(0,0,0,0.5); position: relative; overflow: hidden; }
        .globo-area::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(--primary), var(--success)); }
        .numero-destaque { font-size: 70px; font-weight: 800; margin: 10px 0; color: #fbbf24; line-height: 1.1; text-shadow: 0 4px 20px rgba(251, 191, 36, 0.4); }
        .bolas-sorteadas { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
        .bola { width: 46px; height: 46px; background: linear-gradient(135deg, #ffffff, #e2e8f0); color: #0f172a; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 800; font-size: 14px; box-shadow: 0 4px 6px rgba(0,0,0,0.3); border: 2px solid #cbd5e1; animation: popIn 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275); letter-spacing: -0.5px; }

        @keyframes popIn { 0% { transform: scale(0); } 100% { transform: scale(1); } }

        .painel-cartelas { display: grid; grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); gap: 12px; max-height: 70vh; overflow-y: auto; padding: 15px; background: #f8fafc; border-radius: var(--radius); border: 1px solid var(--border); }
        .cartela-unidade { background: var(--surface); padding: 8px; border-radius: 10px; position: relative; transition: all 0.2s ease; box-shadow: var(--shadow-sm); border: 2px solid transparent; }
        .cartela-titulo { color: var(--text-muted); text-align: center; font-size: 12px; margin-bottom: 6px; font-weight: 800; text-transform: uppercase; letter-spacing: 1px; }
        .cartela-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 3px; }
        .cartela-header { background: var(--primary); color: white; text-align: center; font-weight: 800; padding: 6px 0; font-size: 14px; border-radius: 4px; }
        .cartela-header:nth-child(1) { background: #ef4444; }
        .cartela-header:nth-child(2) { background: #f59e0b; }
        .cartela-header:nth-child(3) { background: #10b981; }
        .cartela-header:nth-child(4) { background: #3b82f6; }
        .cartela-header:nth-child(5) { background: #8b5cf6; }
        
        .cartela-cell { 
            background: #f1f5f9; 
            text-align: center; 
            padding: 8px 0; 
            font-size: 14px; 
            font-weight: 700; 
            border-radius: 4px; 
            cursor: pointer; 
            user-select: none; 
            transition: 0.2s; 
            color: #334155; 
            border: 1px solid #e2e8f0; 
            position: relative; 
        }
        @media(hover: hover) { .cartela-cell:hover:not(.marcada) { background: #e2e8f0; } }
        
        .loja-selecionada { border-color: var(--success); box-shadow: 0 0 0 3px rgba(16, 185, 129, 0.2); transform: translateY(-2px); }
        .cartela-cell.marcada, .cartela-cell.bola-chamada.marcada { background: var(--success); color: white; border-color: #059669; transform: scale(0.95); box-shadow: inset 0 2px 5px rgba(0,0,0,0.3); }
        
        .cartela-cell.bola-chamada { background: #fef08a; border-color: #fde047; color: #713f12; }
        .cell-free { background: #fbbf24; color: #78350f; border-color: #f59e0b; }

        .indicador-sorteado {
            position: absolute; top: 2px; right: 3px; font-size: 9px; font-weight: 800; background: rgba(15, 23, 42, 0.75); color: #fff; padding: 1px 3px; border-radius: 3px; line-height: 1; pointer-events: none; letter-spacing: -0.5px; box-shadow: 0 1px 2px rgba(0,0,0,0.2); display: none;
        }
        .cartela-cell.bola-chamada .indicador-sorteado,
        .cartela-cell.bola-chamada.marcada .indicador-sorteado { display: block; }
        .cartela-cell.marcada .indicador-sorteado { background: rgba(255, 255, 255, 0.85); color: #065f46; }

        .premio-box { border: 2px dashed #fcd34d; padding: 20px; border-radius: var(--radius); text-align: center; background: #fffbeb; margin-bottom: 20px; box-shadow: var(--shadow-sm); }
        .lista-premios-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 8px; margin-top: 10px; }
        .item-premio { background: #ffffff; border: 1px solid #fde68a; padding: 10px; border-radius: 8px; text-align: center; transition: all 0.2s; }
        .item-premio.ativo { border-color: var(--warning); background: #fef3c7; box-shadow: 0 0 0 2px #f59e0b; font-weight: bold; transform: scale(1.02); }
        .item-premio .titulo-p { font-size: 11px; text-transform: uppercase; color: #92400e; font-weight: 800; }
        .item-premio .val-p { font-size: 14px; font-weight: 700; color: var(--text-main); margin-top: 2px; }

        .pix-container { background: #ffffff; padding: 12px; border-radius: 8px; border: 1px solid var(--border); margin-top: 15px; word-break: break-all; font-family: 'Courier New', monospace; font-size: 15px; font-weight: 600; color: var(--text-main); display: flex; align-items: center; justify-content: space-between; gap: 10px; }
        .grito-vitoria-box { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-bottom: 20px; }
        @media(max-width: 600px) { .grito-vitoria-box { grid-template-columns: 1fr; } }
        .btn-grito { margin: 0; font-weight: 800; font-size: 14px; padding: 15px 6px; text-transform: uppercase; box-shadow: var(--shadow-sm); }

        #banner-alerta-bingo, #banner-alerta-bingo-player { background: linear-gradient(135deg, #ef4444, #f59e0b); color: white; padding: 20px; border-radius: var(--radius); text-align: center; margin-bottom: 20px; font-size: 18px; font-weight: 800; box-shadow: var(--shadow-lg); display: none; animation: pulseAlert 1s infinite alternate; }
        @keyframes pulseAlert { 0% { transform: scale(1); } 100% { transform: scale(1.02); } }
        
        #admin-conferencia-area { display: none; background: #fff; padding: 20px; border-radius: var(--radius); margin-bottom: 24px; border: 3px solid var(--warning); box-shadow: var(--shadow-lg); }
        .alerta-item-admin { background: #fffbeb; border: 1px solid #fde68a; padding: 15px; border-radius: 8px; margin-bottom: 15px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }

        .video-wrapper { position: relative; width: 100%; border-radius: var(--radius); overflow: hidden; background: #000; box-shadow: var(--shadow-lg); }
        .video-container { width: 100%; height: 400px; border: none; display: block; }
        @media(min-width: 900px) { .video-container { height: 500px; } }
        .video-placeholder { position: absolute; inset: 0; display: flex; flex-direction: column; align-items: center; justify-content: center; color: #64748b; background: #0f172a; z-index: 1; text-align: center; padding: 20px;}

        .abas-jogador { display: flex; gap: 12px; margin-bottom: 25px; border-bottom: 2px solid var(--border); padding-bottom: 15px; }
        .abas-jogador button { margin: 0; flex: 1; border-radius: 8px; font-size: 16px; padding: 16px; }

        .pedido-card { display: flex; justify-content: space-between; align-items: center; padding: 12px 15px; background: #f8fafc; border: 1px solid var(--border); border-left: 4px solid var(--warning); border-radius: 8px; margin-bottom: 10px; }
        @media(max-width: 600px) { .pedido-card { flex-direction: column; align-items: flex-start; gap: 10px; } .pedido-card div { width: 100%; display: flex; } .pedido-card button { flex: 1; margin: 0; } }

        .card-desempate-item { background: #ffffff; border: 2px solid var(--primary); padding: 15px; border-radius: 10px; text-align: center; }
        .card-desempate-item.vencedor-destaque { border-color: var(--success); background: #ecfdf5; box-shadow: 0 0 0 3px rgba(16, 185, 129, 0.3); }

        #toast-container { position: fixed; bottom: 20px; right: 20px; z-index: 9999; display: flex; flex-direction: column; gap: 10px; }
        .toast { background: white; color: var(--text-main); padding: 16px 24px; border-radius: 8px; box-shadow: 0 10px 25px -5px rgba(0,0,0,0.2); display: flex; align-items: center; gap: 12px; font-weight: 600; transform: translateX(120%); transition: transform 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55); border-left: 4px solid var(--primary); }
        .toast.show { transform: translateX(0); }
        .toast.success { border-left-color: var(--success); }
        .toast.error { border-left-color: var(--danger); }
        .toast.warning { border-left-color: var(--warning); }
        
        .modal-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.6); backdrop-filter: blur(4px); display: flex; align-items: center; justify-content: center; z-index: 9999; opacity: 0; pointer-events: none; transition: opacity 0.2s; }
        .modal-overlay.active { opacity: 1; pointer-events: auto; }
        .modal-content { background: var(--surface); padding: 30px; border-radius: var(--radius); width: 90%; max-width: 400px; box-shadow: var(--shadow-lg); transform: translateY(20px); transition: 0.3s; }
        .modal-overlay.active .modal-content { transform: translateY(0); }

        ::-webkit-scrollbar { width: 8px; height: 8px; }
        ::-webkit-scrollbar-track { background: transparent; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }
        
        .header-painel { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--border); padding-bottom: 20px; margin-bottom: 20px; flex-wrap: wrap; gap: 10px; }
        .btn-sair { width: auto; margin: 0; padding: 8px 16px; font-size: 14px; }
        
        .footer-duartetec { text-align: center; margin-top: auto; padding: 20px 0; color: var(--text-muted); font-size: 14px; font-weight: 600; }
        .footer-duartetec span { color: var(--primary); }
    </style>
</head>
<body>

<div id="toast-container"></div>

<!-- Modal Senha Admin -->
<div class="modal-overlay" id="senha-modal">
    <div class="modal-content">
        <h3><i class="fa-solid fa-lock"></i> Acesso Restrito</h3>
        <p>Digite a senha do administrador:</p>
        <input type="password" id="modal-senha-input" placeholder="Senha..." autocomplete="off" onkeypress="if(event.key === 'Enter') confirmarSenhaAdmin()">
        <div style="display: flex; gap: 10px; margin-top: 20px;">
            <button class="outline" onclick="fecharModalSenha()" style="margin: 0;">Cancelar</button>
            <button class="primary" onclick="confirmarSenhaAdmin()" style="margin: 0;">Entrar</button>
        </div>
    </div>
</div>

<!-- Modal Registro Inicial do Jogador -->
<div class="modal-overlay" id="registro-jogador-modal">
    <div class="modal-content">
        <h3><i class="fa-solid fa-user-plus"></i> Identificação</h3>
        <p>Digite seu nome completo (ou apelido) para entrar no jogo:</p>
        <input type="text" id="modal-nome-jogador-input" placeholder="Seu nome completo..." autocomplete="off" onkeypress="if(event.key === 'Enter') confirmarNomeJogador()">
        <div style="display: flex; gap: 10px; margin-top: 20px;">
            <button class="outline" onclick="fecharModalRegistroJogador()" style="margin: 0;">Cancelar</button>
            <button class="primary" onclick="confirmarNomeJogador()" style="margin: 0;">Entrar no Jogo</button>
        </div>
    </div>
</div>

<!-- Modal Nomes (Apenas Admin/Fallback) -->
<div class="modal-overlay" id="name-modal">
    <div class="modal-content">
        <h3><i class="fa-solid fa-video"></i> Entrar na Transmissão</h3>
        <p>Como você deseja ser chamado na chamada de vídeo?</p>
        <input type="text" id="modal-name-input" placeholder="Digite seu nome..." autocomplete="off" onkeypress="if(event.key === 'Enter') confirmarNomeLive()">
        <div style="display: flex; gap: 10px; margin-top: 20px;">
            <button class="outline" onclick="fecharModalName()" style="margin: 0;">Cancelar</button>
            <button class="primary" onclick="confirmarNomeLive()" style="margin: 0;">Conectar</button>
        </div>
    </div>
</div>

<!-- Modal de Conferência de Cartela Específica (Admin) -->
<div class="modal-overlay" id="conferencia-modal">
    <div class="modal-content" style="max-width: 600px; background: #fff; border: 3px solid var(--warning);">
        <h3 id="conferencia-titulo" style="color: var(--warning); margin-bottom: 5px;"><i class="fa-solid fa-magnifying-glass"></i> Conferir Jogador</h3>
        <p id="conferencia-sub" style="font-size: 14px; margin-top: 0; color: var(--text-muted);">Verifique as cartelas enviadas por este participante.</p>
        
        <div class="painel-cartelas" id="cartelas-conferencia-grid" style="background: #fffbeb; border-color: #fde68a; max-height: 50vh; margin-bottom: 20px;"></div>
        
        <div style="display: flex; gap: 10px;">
            <button class="outline" onclick="document.getElementById('conferencia-modal').classList.remove('active')" style="margin: 0;">Fechar</button>
            <button class="success" id="btn-aprovar-vitoria" style="margin: 0;"><i class="fa-solid fa-check"></i> Validar e Avançar Prémio</button>
        </div>
    </div>
</div>

<!-- Modal de Desempate -->
<div class="modal-overlay" id="desempate-modal">
    <div class="modal-content" style="max-width: 650px; background: #fff; border: 3px solid var(--primary);">
        <h3 style="color: var(--primary); margin-bottom: 5px;"><i class="fa-solid fa-dice-three"></i> Disputa de Desempate (Pedras)</h3>
        <p style="font-size: 14px; margin-top: 0; color: var(--text-muted);">Sorteie as pedras entre os jogadores empatados para definir o vencedor absoluto do prêmio.</p>

        <div style="margin-bottom: 15px;">
            <label style="font-size: 13px; font-weight: 800; display: block; margin-bottom: 4px;">Critério de Vitoria:</label>
            <select id="select-criterio-desempate" style="margin: 0;">
                <option value="maior">Maior Pedra Vence (Quem tirar o número mais alto)</option>
                <option value="menor">Menor Pedra Vence (Quem tirar o número mais baixo)</option>
            </select>
        </div>

        <button class="warning" onclick="sortearPedrasDesempate()" style="margin-bottom: 20px;"><i class="fa-solid fa-shuffle"></i> Sortear Pedras dos Empatados</button>

        <div id="grid-jogadores-desempate" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; margin-bottom: 20px;"></div>

        <div style="display: flex; gap: 10px;">
            <button class="outline" onclick="document.getElementById('desempate-modal').classList.remove('active')" style="margin: 0;">Cancelar</button>
            <button class="success" id="btn-confirmar-vencedor-desempate" style="margin: 0;" disabled onclick="confirmarGanhadorDesempate()"><i class="fa-solid fa-trophy"></i> Confirmar Vencedor Final</button>
        </div>
    </div>
</div>

<!-- Modal de Vencedores Confirmados -->
<div class="modal-overlay" id="vencedor-modal">
    <div class="modal-content" style="max-width: 700px; text-align: center; background: #fffbeb; border: 3px solid #f59e0b;">
        <h2 style="color: #d97706; margin-bottom: 5px; font-size: 26px;"><i class="fa-solid fa-trophy"></i> PRÊMIO CONQUISTADO!</h2>
        <p style="font-weight: 600; color: var(--text-muted); margin-bottom: 15px;">O sistema já está avançando automaticamente para a próxima etapa/rodada!</p>
        
        <div id="lista-vencedores-modal" style="max-height: 55vh; overflow-y: auto; display: flex; flex-direction: column; gap: 15px; margin-bottom: 20px; text-align: left;"></div>
        
        <button class="primary" onclick="document.getElementById('vencedor-modal').classList.remove('active')">Continuar Acompanhando</button>
    </div>
</div>

<div class="container" id="main-container">
    <!-- TELA 1: LOGIN -->
    <div id="tela-login" class="card active" style="text-align: center; max-width: 450px; margin: 80px auto;">
        <div style="font-size: 48px; margin-bottom: 15px; color: var(--primary);"><i class="fa-solid fa-dice"></i></div>
        <h1>Bingo Premium</h1>
        <p style="margin-bottom: 30px;">Bem-vindo ao sistema profissional de bingo da família. Escolha seu perfil para iniciar.</p>
        <button onclick="entrarComo('admin')"><i class="fa-solid fa-crown"></i> Entrar como Administrador</button>
        <button onclick="abrirModalRegistroJogador()" class="outline"><i class="fa-solid fa-user"></i> Entrar como Jogador</button>
    </div>

    <!-- TELA 2: ADMINISTRADOR -->
    <div id="tela-admin" class="card">
        <div class="header-painel">
            <h2 style="margin:0;"><i class="fa-solid fa-sliders"></i> Painel do Administrador (Rodada <span class="display-rodada-texto">1</span>)</h2>
            <div style="display: flex; gap: 10px;">
                <button class="outline btn-sair" onclick="sairParaLogin()"><i class="fa-solid fa-arrow-right-from-bracket"></i> Sair</button>
                <button class="danger btn-sair" onclick="resetarJogo()"><i class="fa-solid fa-rotate-right"></i> Zerar Rodada</button>
            </div>
        </div>

        <div id="banner-alerta-bingo">
            <i class="fa-solid fa-bell-concierge" style="font-size: 28px; margin-right: 10px;"></i>
            <span id="texto-alerta-bingo">JOGADORES GRITARAM BINGO!</span>
        </div>

        <div id="admin-conferencia-area">
            <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; margin-bottom: 15px;">
                <div>
                    <h3 style="margin: 0; color: var(--warning);"><i class="fa-solid fa-users-viewfinder"></i> Fila de Jogadores que Bateram (<span id="qtd-alertas-pendentes">0</span>)</h3>
                    <p style="margin: 5px 0 0 0; font-size: 14px; color: var(--text-muted);">Veja quem bateu, confira a cartela e valide para o sistema avançar automaticamente.</p>
                </div>
                <button class="primary" style="width: auto; margin: 0; background: var(--primary);" onclick="abrirModalDesempate()"><i class="fa-solid fa-dice-three"></i> Disputa de Desempate (Pedras)</button>
            </div>
            
            <div id="lista-alertas-admin"></div>
            <button class="outline" style="margin-top: 10px; background: white; color: var(--danger); width: auto;" onclick="limparAlertasBingo()">Limpar Alertas / Reiniciar</button>
        </div>

        <div class="card" style="padding: 20px; border: 2px solid var(--primary); margin-bottom: 24px;">
            <h3 style="margin-bottom: 15px; color: var(--primary);"><i class="fa-solid fa-cart-shopping"></i> Aprovações de Compra Pendentes</h3>
            <p style="font-size: 14px; margin-top: 0; margin-bottom: 15px;">Confira o PIX e aprove para liberar as cartelas para os jogadores.</p>
            <div id="lista-pedidos-admin">
                <p style="color: var(--text-muted); margin: 0;">Nenhum pedido aguardando aprovação no momento.</p>
            </div>
        </div>

        <div class="game-layout">
            <div>
                <h3>Prêmios e Ciclo de Rodadas</h3>
                <div class="card" style="padding: 20px; background: #f8fafc; margin-bottom: 24px;">
                    <div style="background: #eef2ff; padding: 10px; border-radius: 8px; margin-bottom: 15px; font-weight: bold; color: var(--primary); text-align: center;">
                        Rodada Atual: <span class="display-rodada-texto">1</span>
                    </div>

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">1º Prêmio:</label>
                    <input type="text" id="admin-p1" placeholder="Ex: R$ 50,00" style="padding: 8px 12px; font-size: 14px;">

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">2º Prêmio:</label>
                    <input type="text" id="admin-p2" placeholder="Ex: R$ 100,00" style="padding: 8px 12px; font-size: 14px;">

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">3º Prêmio:</label>
                    <input type="text" id="admin-p3" placeholder="Ex: R$ 150,00" style="padding: 8px 12px; font-size: 14px;">

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">4º Prêmio (Bingo Cheio):</label>
                    <input type="text" id="admin-p4" placeholder="Ex: TV 32' ou R$ 500,00" style="padding: 8px 12px; font-size: 14px;">

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px; margin-top: 10px;">Etapa em Disputa (Automática):</label>
                    <select id="admin-etapa-ativa">
                        <option value="1">1º Prêmio</option>
                        <option value="2">2º Prêmio</option>
                        <option value="3">3º Prêmio</option>
                        <option value="4">4º Prêmio (Bingo Cheio)</option>
                    </select>

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">Valor Unitário da Cartela (R$):</label>
                    <input type="text" id="admin-valor-cartela" placeholder="Ex: 10,00" style="padding: 8px 12px; font-size: 14px;">

                    <label style="font-weight: 600; font-size: 13px; display: block; margin-bottom: 4px;">Chave PIX:</label>
                    <input type="text" id="admin-pix" value="16d7166d-3c78-41a9-9a29-51bef4f01ffe" style="padding: 8px 12px; font-size: 14px;">
                    
                    <button class="success" onclick="salvarConfiguracoes()" style="margin: 0; margin-top: 10px;"><i class="fa-solid fa-floppy-disk"></i> Salvar e Sincronizar</button>
                </div>

                <h3>Câmera Principal (Host)</h3>
                <div class="video-wrapper">
                    <div class="video-placeholder" id="admin-video-placeholder">
                        <i class="fa-solid fa-video-slash" style="font-size: 32px; margin-bottom: 10px;"></i>
                        <p>Câmera Desligada</p>
                    </div>
                    <div id="admin-video"></div>
                </div>
                <button onclick="prepararLive('admin')" style="margin-top: 15px;"><i class="fa-solid fa-video"></i> Iniciar Transmissão</button>
            </div>
            <div>
                <div class="globo-area">
                    <div style="font-size: 14px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: #94a3b8;">Última Bola Sorteada (Pública)</div>
                    <div class="numero-destaque" id="bola-atual">--</div>
                    <button class="success" onclick="sortearBola()" style="font-size: 20px; padding: 20px; margin-top: 20px; box-shadow: var(--shadow-lg);">
                        <i class="fa-solid fa-shuffle"></i> Sortear Novo Número
                    </button>

                    <div id="painel-liberacao" style="display: none; margin-top: 20px; background: rgba(0,0,0,0.3); padding: 15px; border-radius: 8px; border: 2px dashed #fbbf24; text-align: center;">
                        <div style="font-size: 13px; color: #fbbf24; font-weight: bold; margin-bottom: 5px;">Sorteada (Aguardando Sua Liberação):</div>
                        <div id="bola-pendente-admin" style="font-size: 50px; font-weight: 800; color: #fbbf24; margin: 5px 0;">--</div>
                        <button class="warning" onclick="liberarBolaParaJogadores()" style="margin-top: 10px; font-weight: bold; font-size: 16px; padding: 14px; width: 100%;"><i class="fa-solid fa-bullhorn"></i> Liberar Pedra para os Jogadores</button>
                    </div>
                </div>
                
                <div style="display: flex; justify-content: space-between; align-items: center;">
                    <h4 style="margin: 0;">Histórico de Bolas</h4>
                    <span style="background: var(--primary); color: white; padding: 4px 12px; border-radius: 20px; font-weight: bold; font-size: 14px;"><span id="qtd-sorteadas">0</span>/75</span>
                </div>
                <div class="bolas-sorteadas" id="lista-bolas-admin"></div>
            </div>
        </div>
    </div>

    <!-- TELA 3: JOGADOR -->
    <div id="tela-jogador" class="card">
        <div class="header-painel">
            <h2 style="margin:0;"><i class="fa-solid fa-ticket"></i> Área de: <span id="display-nome-jogador" style="color: var(--primary);">Jogador</span></h2>
            <div style="display: flex; gap: 15px; align-items: center;">
                <div id="status-conexao" style="font-size: 14px; font-weight: 600; color: var(--success);"><i class="fa-solid fa-circle-check"></i> Sincronizado ao Vivo</div>
                <button class="outline btn-sair" style="border-color: var(--danger); color: var(--danger);" onclick="sairParaLogin()"><i class="fa-solid fa-arrow-right-from-bracket"></i> Sair</button>
            </div>
        </div>

        <div id="banner-alerta-bingo-player">
            <i class="fa-solid fa-bullhorn"></i> <span id="texto-alerta-player">ALGUÉM GRITOU BINGO NA SALA!</span>
            <p style="font-size: 14px; margin-top: 5px; font-weight: 400;">Acompanhe os vencedores confirmados.</p>
        </div>

        <div class="abas-jogador">
            <button id="btn-nav-loja" class="warning" onclick="mudarModoJogador('loja')"><i class="fa-solid fa-shop"></i> 1. Loja & Pagamentos</button>
            <button id="btn-nav-jogo" class="outline" onclick="mudarModoJogador('jogo')"><i class="fa-solid fa-gamepad"></i> 2. Sala de Jogo (Ao Vivo)</button>
        </div>

        <div id="modo-loja">
            <div class="game-layout">
                <div>
                    <h3>Passo a Passo</h3>
                    <div class="premio-box">
                        <div style="color: var(--warning); font-size: 24px; margin-bottom: 5px;"><i class="fa-solid fa-trophy"></i> Rodada <span class="display-rodada-texto">1</span> - Prêmios</div>
                        <p id="player-valor-cartela-info" style="margin: 0 0 10px 0; font-weight: 800; color: var(--primary); font-size: 16px;">Valor por cartela: R$ 0,00</p>
                        
                        <div class="lista-premios-grid" id="player-premios-grid">
                            <div class="item-premio" id="p-box-1"><div class="titulo-p">1º Prêmio</div><div class="val-p" id="p-val-1">-</div></div>
                            <div class="item-premio" id="p-box-2"><div class="titulo-p">2º Prêmio</div><div class="val-p" id="p-val-2">-</div></div>
                            <div class="item-premio" id="p-box-3"><div class="titulo-p">3º Prêmio</div><div class="val-p" id="p-val-3">-</div></div>
                            <div class="item-premio" id="p-box-4"><div class="titulo-p">4º Bingo</div><div class="val-p" id="p-val-4">-</div></div>
                        </div>

                        <div class="pix-container" style="border-color: #fde68a;">
                            <span id="player-pix" style="flex: 1; text-align: left; overflow-wrap: break-word;">16d7166d-3c78-41a9-9a29-51bef4f01ffe</span>
                            <button class="outline" style="width: auto; margin: 0; padding: 8px 12px; background: white;" onclick="copiarPix()" title="Copiar PIX"><i class="fa-solid fa-copy"></i> Copiar</button>
                        </div>
                    </div>
                </div>

                <div>
                    <div style="display: flex; justify-content: space-between; align-items: flex-end; margin-bottom: 15px; flex-wrap: wrap; gap: 10px;">
                        <div>
                            <h3 style="margin: 0;">Vitrine de Cartelas</h3>
                            <p style="margin: 5px 0 0 0; font-size: 14px;">Selecione para comprar.</p>
                        </div>
                        <div style="font-weight: 800; font-size: 18px; color: var(--primary); background: #eef2ff; padding: 8px 15px; border-radius: 8px;">
                            <span id="qtd-selecionadas">0</span> sel. (<span id="total-preco-selecionado">R$ 0,00</span>)
                        </div>
                    </div>
                    
                    <div class="painel-cartelas" id="vitrine-cartelas" style="max-height: 55vh;"></div>
                    
                    <button id="btn-confirmar-compra" class="success" style="margin-top: 20px; font-size: 18px; padding: 20px; box-shadow: var(--shadow-lg);" onclick="enviarPedido()">
                        <i class="fa-solid fa-check-circle"></i> Solicitar Aprovação da Compra
                    </button>
                </div>
            </div>
        </div>

        <div id="modo-jogo" style="display: none;">
            <div class="game-layout" id="player-layout-jogo">
                <div id="coluna-esquerda-jogo">
                    <div class="globo-area" style="padding: 20px 15px; margin-bottom: 20px;">
                        <div style="font-size: 12px; font-weight: bold; text-transform: uppercase; color: #94a3b8;">Rodada <span class="display-rodada-texto">1</span> - Última Pedra Liberada</div>
                        <div class="numero-destaque" id="player-bola-atual" style="font-size: 55px; margin: 5px 0;">--</div>
                        <div class="bolas-sorteadas" id="lista-bolas-player" style="justify-content: center; max-height: 110px; overflow-y: auto; background: rgba(0,0,0,0.2); padding: 10px; border-radius: 8px;"></div>
                    </div>

                    <div class="grito-vitoria-box">
                        <button class="danger btn-grito" onclick="gritarVitoria('PAROUU!')"><i class="fa-solid fa-hand"></i> Parouu!</button>
                        <button class="warning btn-grito" onclick="gritarVitoria('BATIIU!')"><i class="fa-solid fa-bolt"></i> Batiii!</button>
                        <button class="success btn-grito" onclick="gritarVitoria('BINGOOOO!')"><i class="fa-solid fa-trophy"></i> Bingooo!</button>
                    </div>

                    <div class="video-wrapper" style="margin-top: 24px;">
                        <div class="video-placeholder" id="player-video-placeholder">
                            <i class="fa-solid fa-users" style="font-size: 32px; margin-bottom: 10px;"></i>
                            <p>Aguardando câmera familiar...</p>
                        </div>
                        <div id="player-video"></div>
                    </div>
                    <button class="outline" onclick="prepararLive('jogador')" style="margin-top: 15px;"><i class="fa-solid fa-video"></i> Ligar minha Câmera</button>
                </div>

                <div id="coluna-direita-jogo">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; flex-wrap: wrap; gap: 10px;">
                        <div>
                            <h3 style="margin-bottom: 5px;">Suas Cartelas (<span id="qtd-minhas-cartelas">0</span>)</h3>
                            <p style="margin-top: 0; font-size: 14px;">Clique nas dezenas sorteadas para marcar.</p>
                        </div>
                        
                        <div style="display: flex; gap: 10px;">
                            <button class="warning" style="width: auto; padding: 8px 15px; margin: 0; font-size: 14px;" onclick="desmarcarTodasCartelas()">
                                <i class="fa-solid fa-eraser"></i> Limpar Marcações
                            </button>
                            <button id="btn-expandir-jogo" class="outline" style="width: auto; padding: 8px 15px; margin: 0; font-size: 14px;" onclick="toggleExpandirCartelasJogo()">
                                <i class="fa-solid fa-expand"></i> Focar
                            </button>
                        </div>
                    </div>
                    
                    <div class="painel-cartelas" id="minhas-cartelas-area" style="background: #e0e7ff; border-color: #c7d2fe; min-height: 60vh;">
                        <div style="grid-column: 1 / -1; display: flex; flex-direction: column; align-items: center; justify-content: center; color: #64748b; padding: 40px 20px; text-align: center;">
                            <i class="fa-solid fa-ticket" style="font-size: 48px; margin-bottom: 15px; color: #cbd5e1;"></i>
                            <p>Você não possui cartelas aprovadas para jogar no momento.</p>
                            <button class="primary" style="width: auto; margin-top: 15px;" onclick="mudarModoJogador('loja')">Ir para a Loja</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
    
    <div class="footer-duartetec">Desenvolvido por <span>DuarteTec</span></div>
</div>

<script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.1/firebase-app.js";
    import { getDatabase, ref, set, update, onValue, remove, get } from "https://www.gstatic.com/firebasejs/10.8.1/firebase-database.js";

    const firebaseConfig = {
        apiKey: "AIzaSyD5HkQ0cP5zNIH46jLqrdbJKhKOlq_zf6o",
        authDomain: "bingofamilia-ed230.firebaseapp.com",
        projectId: "bingofamilia-ed230",
        storageBucket: "bingofamilia-ed230.firebasestorage.app",
        messagingSenderId: "272815257252",
        appId: "1:272815257252:web:a3ba8526232a32bd7ed831",
        measurementId: "G-YWWDRN9MSF"
    };

    const app = initializeApp(firebaseConfig);
    const db = getDatabase(app);

    let bolasDisponiveis = Array.from({length: 75}, (_, i) => i + 1);
    let bolasSorteadas = [];
    let bolaPendenteAtual = null;
    const SALA_MEET = "BingoPremiumFamiliaExclusivo2026";
    let roleParaLive = '';

    let cartelasDaLoja = [];
    let cartelasSelecionadas = []; 
    let minhasCartelasCompradas = []; 
    let valorUnitarioCartela = 10.00; 

    let meuJogadorId = 'jogador_' + Math.random().toString(36).substr(2, 9);
    let nomeJogadorAtual = ''; 
    let desempateLista = []; 
    let vencedorDesempateAtual = null;

    function showToast(message, type = 'success') {
        const container = document.getElementById('toast-container');
        const toast = document.createElement('div');
        toast.className = `toast ${type}`;
        
        let icon = 'fa-check-circle';
        if(type === 'error') icon = 'fa-circle-xmark';
        if(type === 'warning') icon = 'fa-triangle-exclamation';
        if(type === 'info') icon = 'fa-circle-info';
        
        toast.innerHTML = `<i class="fa-solid ${icon}" style="font-size: 20px;"></i> <span>${message}</span>`;
        container.appendChild(toast);
        
        setTimeout(() => toast.classList.add('show'), 10);
        setTimeout(() => { 
            toast.classList.remove('show'); 
            setTimeout(() => toast.remove(), 300); 
        }, 4000);
    }

    function formatarBola(num) {
        if (!num || num === '--') return '--';
        if (num <= 15) return 'B - ' + num;
        if (num <= 30) return 'I - ' + num;
        if (num <= 45) return 'N - ' + num;
        if (num <= 60) return 'G - ' + num;
        return 'O - ' + num;
    }

    function abrirModalRegistroJogador() {
        document.getElementById('registro-jogador-modal').classList.add('active');
        setTimeout(() => document.getElementById('modal-nome-jogador-input').focus(), 100);
    }

    function fecharModalRegistroJogador() {
        document.getElementById('registro-jogador-modal').classList.remove('active');
    }

    function confirmarNomeJogador() {
        const nome = document.getElementById('modal-nome-jogador-input').value.trim();
        if(!nome) return showToast("Por favor, digite seu nome ou apelido!", "error");
        
        nomeJogadorAtual = nome;
        document.getElementById('display-nome-jogador').innerText = nomeJogadorAtual;
        fecharModalRegistroJogador();
        entrarComo('jogador');
    }

    function entrarComo(perfil) {
        if(perfil === 'admin') {
            document.getElementById('senha-modal').classList.add('active');
            setTimeout(() => document.getElementById('modal-senha-input').focus(), 100);
        } else {
            document.getElementById('tela-login').classList.remove('active');
            document.getElementById('tela-jogador').classList.add('active');
            gerarLojaDeCartelas(); 
            showToast(`Bem-vindo, ${nomeJogadorAtual}!`, "success");
        }
    }

    function sairParaLogin() {
        document.getElementById('tela-admin').classList.remove('active');
        document.getElementById('tela-jogador').classList.remove('active');
        document.getElementById('tela-login').classList.add('active');
        
        document.getElementById('admin-video').innerHTML = '';
        document.getElementById('player-video').innerHTML = '';
        document.getElementById('admin-video-placeholder').style.display = 'flex';
        document.getElementById('player-video-placeholder').style.display = 'flex';
        
        showToast("Sessão encerrada.", "info");
    }

    function fecharModalSenha() {
        document.getElementById('senha-modal').classList.remove('active');
        document.getElementById('modal-senha-input').value = '';
    }

    function confirmarSenhaAdmin() {
        const senha = document.getElementById('modal-senha-input').value;
        if(senha === 'Chefe123') {
            fecharModalSenha();
            document.getElementById('tela-login').classList.remove('active');
            document.getElementById('tela-admin').classList.add('active');
            showToast("Bem-vindo ao Painel Administrativo", "info");
        } else {
            showToast("Senha incorreta!", "error");
            document.getElementById('modal-senha-input').value = '';
            document.getElementById('modal-senha-input').focus();
        }
    }

    function copiarPix() {
        navigator.clipboard.writeText(document.getElementById('player-pix').innerText).then(() => { 
            showToast("Chave PIX copiada!", "success"); 
        });
    }

    function desmarcarTodasCartelas() {
        const marcadas = document.querySelectorAll('#minhas-cartelas-area .cartela-cell.marcada');
        if(marcadas.length === 0) {
            showToast("Suas cartelas já estão limpas!", "info");
            return;
        }
        marcadas.forEach(cell => cell.classList.remove('marcada'));
        showToast("Todas as marcações foram limpas!", "success");
    }

    function criarObjetoCartela(id) {
        const ranges = [[1,15], [16,30], [31,45], [46,60], [61,75]];
        let colunas = [[], [], [], [], []];
        for(let c=0; c<5; c++) {
            while(colunas[c].length < 5) {
                let num = Math.floor(Math.random() * (ranges[c][1] - ranges[c][0] + 1)) + ranges[c][0];
                if(!colunas[c].includes(num)) colunas[c].push(num);
            }
        }
        return { id: id, colunas: colunas };
    }

    function verificarCartelaCompleta(cartela, bolas) {
        let colunas = cartela.colunas; 
        
        const isMarked = (c, r) => {
            if (r === 2 && c === 2) return true; 
            let num = colunas[c][r];
            return bolas.includes(num);
        };

        for (let r = 0; r < 5; r++) {
            let rowComplete = true;
            for (let c = 0; c < 5; c++) {
                if (!isMarked(c, r)) { rowComplete = false; break; }
            }
            if (rowComplete) return true;
        }

        for (let c = 0; c < 5; c++) {
            let colComplete = true;
            for (let r = 0; r < 5; r++) {
                if (!isMarked(c, r)) { colComplete = false; break; }
            }
            if (colComplete) return true;
        }

        let diag1Complete = true;
        for (let i = 0; i < 5; i++) {
            if (!isMarked(i, i)) { diag1Complete = false; break; }
        }
        if (diag1Complete) return true;

        let diag2Complete = true;
        for (let i = 0; i < 5; i++) {
            if (!isMarked(4 - i, i)) { diag2Complete = false; break; }
        }
        if (diag2Complete) return true;

        const quatroCantosComplete = isMarked(0, 0) && isMarked(4, 0) && isMarked(0, 4) && isMarked(4, 4);
        if (quatroCantosComplete) return true;

        return false;
    }

    function renderizarHtmlCartela(cartela, modo) {
        const letras = ['B', 'I', 'N', 'G', 'O'];
        let html = `<div class="cartela-unidade" id="${modo}-cartela-${cartela.id}" ${modo === 'loja' ? `onclick="toggleSelecaoLoja(${cartela.id})"` : ''}>`;
        html += `<div class="cartela-titulo">Cartela #${cartela.id.toString().padStart(3, '0')}</div><div class="cartela-grid">`;
        
        letras.forEach(l => html += `<div class="cartela-header">${l}</div>`);
        
        for(let row=0; row<5; row++) {
            for(let col=0; col<5; col++) {
                if(row === 2 && col === 2) { 
                    html += `<div class="cartela-cell cell-free"><i class="fa-solid fa-star"></i></div>`; 
                } else {
                    let num = cartela.colunas[col][row];
                    if(modo === 'loja' || modo === 'conferencia') { 
                        html += `<div class="cartela-cell">${num}</div>`; 
                    } else { 
                        html += `<div class="cartela-cell num-interativo" onclick="this.classList.toggle('marcada')">${num}<span class="indicador-sorteado">Saiu</span></div>`; 
                    }
                }
            }
        }
        html += `</div></div>`;
        return html;
    }

    function renderizarHtmlCartelaParaVencedor(cartela) {
        const letras = ['B', 'I', 'N', 'G', 'O'];
        let html = `<div class="cartela-unidade" style="transform: scale(0.85); transform-origin: top center; margin: -5px; background: #fff; border: 2px solid var(--success);">`;
        html += `<div class="cartela-titulo" style="color: var(--success);"><i class="fa-solid fa-star"></i> Cartela Premiada #${cartela.id.toString().padStart(3, '0')}</div><div class="cartela-grid">`;
        letras.forEach(l => html += `<div class="cartela-header" style="font-size: 11px; padding: 3px 0;">${l}</div>`);
        
        for(let row=0; row<5; row++) {
            for(let col=0; col<5; col++) {
                if(row === 2 && col === 2) { 
                    html += `<div class="cartela-cell cell-free" style="padding: 5px 0; font-size: 11px;"><i class="fa-solid fa-star"></i></div>`; 
                } else {
                    let num = cartela.colunas[col][row];
                    let classeExtra = bolasSorteadas.includes(num) ? 'marcada bola-chamada' : '';
                    html += `<div class="cartela-cell ${classeExtra}" style="padding: 5px 0; font-size: 11px;">${num}</div>`;
                }
            }
        }
        html += `</div></div>`;
        return html;
    }

    function gerarLojaDeCartelas() {
        cartelasDaLoja = [];
        const vitrine = document.getElementById('vitrine-cartelas');
        vitrine.innerHTML = '';
        
        for(let i = 1; i <= 100; i++) {
            let novaCartela = criarObjetoCartela(i);
            cartelasDaLoja.push(novaCartela);
            vitrine.innerHTML += renderizarHtmlCartela(novaCartela, 'loja');
        }
    }

    function toggleSelecaoLoja(id) {
        const el = document.getElementById(`loja-cartela-${id}`);
        if(cartelasSelecionadas.includes(id)) {
            cartelasSelecionadas = cartelasSelecionadas.filter(i => i !== id);
            el.classList.remove('loja-selecionada');
        } else {
            cartelasSelecionadas.push(id);
            el.classList.add('loja-selecionada');
        }
        
        document.getElementById('qtd-selecionadas').innerText = cartelasSelecionadas.length;
        document.getElementById('total-preco-selecionado').innerText = `R$ ${(cartelasSelecionadas.length * valorUnitarioCartela).toFixed(2).replace('.', ',')}`;
    }

    function enviarPedido() {
        if(cartelasSelecionadas.length === 0) { 
            showToast("Selecione pelo menos uma cartela.", "warning"); 
            return; 
        }

        const totalPagamento = cartelasSelecionadas.length * valorUnitarioCartela;
        const cartelasCompletas = cartelasSelecionadas.map(id => cartelasDaLoja.find(c => c.id === id));
        
        set(ref(db, `bingo/pedidos/${meuJogadorId}`), {
            nome: nomeJogadorAtual,
            total: totalPagamento,
            cartelas: cartelasCompletas,
            status: 'pendente',
            timestamp: Date.now()
        });
        
        showToast("Pedido enviado! O Admin está conferindo seu PIX...", "info");
        
        document.getElementById('vitrine-cartelas').innerHTML = `
            <div style="grid-column: 1/-1; text-align: center; padding: 40px; background: #fffbeb; border-radius: 8px; border: 1px solid #fde68a;">
                <i class="fa-solid fa-clock-rotate-left" style="font-size: 40px; color: var(--warning); margin-bottom: 15px;"></i>
                <h3 style="margin-bottom: 10px;">Aguardando Aprovação</h3>
                <p>O administrador está verificando o pagamento de <strong>R$ ${totalPagamento.toFixed(2).replace('.', ',')}</strong>.<br>Assim que aprovado, suas cartelas serão liberadas automaticamente.</p>
            </div>`;
        document.getElementById('btn-confirmar-compra').style.display = 'none';
    }

    function atualizarAreaDeJogo() {
        const area = document.getElementById('minhas-cartelas-area');
        document.getElementById('qtd-minhas-cartelas').innerText = minhasCartelasCompradas.length;
        if(minhasCartelasCompradas.length === 0) return;
        
        area.innerHTML = '';
        minhasCartelasCompradas.forEach(cartela => { 
            area.innerHTML += renderizarHtmlCartela(cartela, 'jogo'); 
        });
        
        document.querySelectorAll('#minhas-cartelas-area .num-interativo').forEach(cell => {
            const num = parseInt(cell.innerText);
            if(bolasSorteadas.includes(num)) { 
                cell.classList.add('bola-chamada'); 
            }
        });
    }

    function mudarModoJogador(modo) {
        if(modo === 'loja') {
            document.getElementById('modo-loja').style.display = 'block';
            document.getElementById('modo-jogo').style.display = 'none';
            document.getElementById('btn-nav-loja').className = 'warning'; 
            document.getElementById('btn-nav-jogo').className = 'outline';
            if(document.getElementById('coluna-esquerda-jogo').style.display === 'none') {
                toggleExpandirCartelasJogo();
            }
        } else {
            document.getElementById('modo-loja').style.display = 'none';
            document.getElementById('modo-jogo').style.display = 'block';
            document.getElementById('btn-nav-loja').className = 'outline'; 
            document.getElementById('btn-nav-jogo').className = 'success';
        }
    }

    function toggleExpandirCartelasJogo() {
        const colEsquerda = document.getElementById('coluna-esquerda-jogo');
        const layout = document.getElementById('player-layout-jogo');
        const container = document.getElementById('main-container');
        const btn = document.getElementById('btn-expandir-jogo');

        if (colEsquerda.style.display === 'none') {
            colEsquerda.style.display = 'block'; 
            layout.style.display = 'grid'; 
            container.classList.remove('expandida');
            btn.innerHTML = '<i class="fa-solid fa-expand"></i> Focar'; 
            btn.className = 'outline';
        } else {
            colEsquerda.style.display = 'none'; 
            layout.style.display = 'block'; 
            container.classList.add('expandida');
            btn.innerHTML = '<i class="fa-solid fa-compress"></i> Voltar'; 
            btn.className = 'primary';
            showToast("Modo foco ativado!", "info");
        }
    }

    function resolverPedido(id, novoStatus) {
        update(ref(db, `bingo/pedidos/${id}`), { status: novoStatus });
    }

    function salvarConfiguracoes() {
        const valorInput = parseFloat(document.getElementById('admin-valor-cartela').value.replace(',', '.')) || 10.00;
        
        get(ref(db, 'bingo/config')).then((snap) => {
            const currentRodada = snap.exists() ? (snap.val().rodadaAtual || 1) : 1;
            
            set(ref(db, 'bingo/config'), { 
                p1: document.getElementById('admin-p1').value || '-',
                p2: document.getElementById('admin-p2').value || '-',
                p3: document.getElementById('admin-p3').value || '-',
                p4: document.getElementById('admin-p4').value || '-',
                etapaAtiva: document.getElementById('admin-etapa-ativa').value,
                rodadaAtual: currentRodada,
                valorCartela: valorInput, 
                pix: document.getElementById('admin-pix').value 
            });
            showToast("Prêmios e configurações salvas!", "success");
        });
    }

    function sortearBola() {
        if(bolasDisponiveis.length === 0) return showToast("Todas sorteadas!", "warning");
        
        get(ref(db, 'bingo/estado')).then((snapshot) => {
            const est = snapshot.val() || {};
            if(est.bolaPendente) {
                showToast("Você já tem uma pedra sorteada aguardando liberação!", "warning");
                return;
            }

            let c = 0; 
            let suspense = setInterval(() => {
                document.getElementById('bola-pendente-admin').innerText = formatarBola(Math.floor(Math.random() * 75) + 1);
                document.getElementById('painel-liberacao').style.display = 'block';
                if(c++ > 15) { 
                    clearInterval(suspense); 
                    finalizarSorteioAdmin(); 
                }
            }, 50);
        });
    }

    function finalizarSorteioAdmin() {
        const bola = bolasDisponiveis.splice(Math.floor(Math.random() * bolasDisponiveis.length), 1)[0];
        
        set(ref(db, 'bingo/estado'), { 
            bolasSorteadas: bolasSorteadas, 
            bolasDisponiveis: bolasDisponiveis,
            bolaPendente: bola
        });
        showToast("Nova pedra sorteada! Clique em 'Liberar Pedra' quando quiser mostrar aos jogadores.", "info");
    }

    window.liberarBolaParaJogadores = function() {
        get(ref(db, 'bingo/estado')).then((snapshot) => {
            const est = snapshot.val() || {};
            if(!est.bolaPendente) return;

            const bola = est.bolaPendente;
            let sorteadas = est.bolasSorteadas || [];
            sorteadas.push(bola);
            
            set(ref(db, 'bingo/estado'), {
                bolasSorteadas: sorteadas,
                bolasDisponiveis: est.bolasDisponiveis,
                bolaPendente: null
            });
            
            showToast(`Pedra ${formatarBola(bola)} liberada para todos os jogadores!`, "success");
        });
    }

    function resetarJogo() {
        if(confirm("Deseja zerar as bolas sorteadas da rodada? As cartelas dos jogadores serão preservadas.")) {
            set(ref(db, 'bingo/estado'), { 
                bolasSorteadas: [], 
                bolasDisponiveis: Array.from({length: 75}, (_, i) => i + 1),
                bolaPendente: null
            });
            remove(ref(db, 'bingo/alertas'));
            remove(ref(db, 'bingo/vencedores'));
            showToast("Rodada zerada para o próximo prêmio!", "success");
        }
    }

    function gritarVitoria(tipo) {
        if(minhasCartelasCompradas.length === 0) { 
            showToast("Sem cartelas ativas!", "warning"); 
            return; 
        }
        
        const cartelasVencedoras = minhasCartelasCompradas.filter(cartela => verificarCartelaCompleta(cartela, bolasSorteadas));

        if(cartelasVencedoras.length === 0) {
            showToast("Nenhuma das suas cartelas completou uma jogada válida com as bolas sorteadas até agora!", "warning");
            return;
        }
        
        const ultimaBolaSorteada = bolasSorteadas.length > 0 ? bolasSorteadas[bolasSorteadas.length - 1] : 0;

        set(ref(db, `bingo/alertas/${meuJogadorId}`), { 
            id: meuJogadorId,
            gritou: true, 
            tipo: tipo, 
            jogador: nomeJogadorAtual, 
            cartelas: cartelasVencedoras, 
            pedra: ultimaBolaSorteada,
            tempoGrito: Date.now(),
            status: 'analise'
        });
        showToast(`Alerta enviado (${tipo})! Apenas sua(s) cartela(s) premiada(s) foram enviadas para conferência.`, "success");
    }

    window.abrirConferenciaJogador = function(jogadorId) {
        get(ref(db, `bingo/alertas/${jogadorId}`)).then((snapshot) => {
            const alerta = snapshot.val();
            if(alerta) {
                document.getElementById('conferencia-titulo').innerHTML = `<i class="fa-solid fa-magnifying-glass"></i> Conferir: ${alerta.jogador} (${alerta.tipo})`;
                document.getElementById('conferencia-sub').innerText = `Pedra no momento do grito: ${formatarBola(alerta.pedra)} | Horário: ${new Date(alerta.tempoGrito).toLocaleTimeString()}`;
                
                const grid = document.getElementById('cartelas-conferencia-grid');
                grid.innerHTML = '';
                alerta.cartelas.forEach(c => {
                    grid.innerHTML += renderizarHtmlCartela(c, 'conferencia');
                });
                
                document.querySelectorAll('#cartelas-conferencia-grid .cartela-cell').forEach(cell => {
                    if(bolasSorteadas.includes(parseInt(cell.innerText))) cell.classList.add('marcada', 'bola-chamada');
                });

                document.getElementById('btn-aprovar-vitoria').onclick = function() {
                    confirmarVencedor(alerta);
                };

                document.getElementById('conferencia-modal').classList.add('active');
            }
        });
    }

    function confirmarVencedor(alerta, detalhesDesempate = null) {
        const tempoConfirmacao = Date.now();
        
        get(ref(db, 'bingo/config')).then((snapConfig) => {
            const cfg = snapConfig.val() || {};
            const etapa = parseInt(cfg.etapaAtiva || '1');
            const rodada = parseInt(cfg.rodadaAtual || '1');
            const premioTexto = cfg[`p${etapa}`] || `Prêmio ${etapa}`;

            set(ref(db, `bingo/vencedores/${alerta.id}_r${rodada}_e${etapa}`), {
                id: alerta.id,
                jogador: alerta.jogador,
                tipo: alerta.tipo,
                pedra: alerta.pedra,
                cartelas: alerta.cartelas,
                premioGanho: premioTexto,
                etapa: etapa,
                rodada: rodada,
                detalhesDesempate: detalhesDesempate,
                tempoGrito: alerta.tempoGrito,
                tempoConfirmacao: tempoConfirmacao
            });

            remove(ref(db, `bingo/alertas/${alerta.id}`));
            document.getElementById('conferencia-modal').classList.remove('active');

            if (etapa < 4) {
                let proximaEtapa = etapa + 1;
                update(ref(db, 'bingo/config'), { etapaAtiva: proximaEtapa.toString() });
                showToast(`🏆 Vitória confirmada (${premioTexto})! O sistema avançou automaticamente para o ${proximaEtapa}º Prêmio da Rodada ${rodada}.`, "success");
            } else {
                let proximaRodada = rodada + 1;
                
                set(ref(db, 'bingo/estado'), { 
                    bolasSorteadas: [], 
                    bolasDisponiveis: Array.from({length: 75}, (_, i) => i + 1),
                    bolaPendente: null
                });
                remove(ref(db, 'bingo/alertas'));
                remove(ref(db, 'bingo/vencedores'));

                update(ref(db, 'bingo/config'), { 
                    etapaAtiva: '1', 
                    rodadaAtual: proximaRodada 
                });

                showToast(`🎉 4º Prêmio finalizado! Fim da Rodada ${rodada}. Iniciando AUTOMATICAMENTE a **Rodada ${proximaRodada}** (1º Prêmio)!`, "success");
            }
        });
    }

    window.abrirModalDesempate = function() {
        get(ref(db, 'bingo/alertas')).then((snapshot) => {
            const alertas = snapshot.val();
            if(!alertas || Object.keys(alertas).length < 2) {
                showToast("É necessário ter pelo menos 2 jogadores na fila para realizar um desempate!", "warning");
                return;
            }

            desempateLista = Object.values(alertas);
            const grid = document.getElementById('grid-jogadores-desempate');
            grid.innerHTML = '';

            desempateLista.forEach(item => {
                grid.innerHTML += `
                <div class="card-desempate-item" id="card-des-${item.id}">
                    <h4 style="margin-bottom: 5px;">${item.jogador}</h4>
                    <p style="font-size: 12px; margin-top: 0; color: var(--text-muted);">${item.tipo}</p>
                    <div class="numero-destaque" id="pedra-des-${item.id}" style="font-size: 40px;">--</div>
                </div>`;
            });

            document.getElementById('btn-confirmar-vencedor-desempate').disabled = true;
            vencedorDesempateAtual = null;
            document.getElementById('desempate-modal').classList.add('active');
        });
    }

    window.sortearPedrasDesempate = function() {
        const criterio = document.getElementById('select-criterio-desempate').value;
        let pedrasUsadas = [];

        desempateLista.forEach(item => {
            let sorteio;
            do {
                sorteio = Math.floor(Math.random() * 75) + 1;
            } while(pedrasUsadas.includes(sorteio));
            
            pedrasUsadas.push(sorteio);
            item.pedraDesempate = sorteio;
            document.getElementById(`pedra-des-${item.id}`).innerText = formatarBola(sorteio);
        });

        if(criterio === 'maior') {
            desempateLista.sort((a,b) => b.pedraDesempate - a.pedraDesempate);
        } else {
            desempateLista.sort((a,b) => a.pedraDesempate - b.pedraDesempate);
        }

        vencedorDesempateAtual = desempateLista[0];

        desempateLista.forEach(item => {
            const el = document.getElementById(`card-des-${item.id}`);
            if(item.id === vencedorDesempateAtual.id) {
                el.classList.add('vencedor-destaque');
            } else {
                el.classList.remove('vencedor-destaque');
            }
        });

        document.getElementById('btn-confirmar-vencedor-desempate').disabled = false;
        showToast(`Sorteio concluído! Campeão pelo critério de pedra ${criterio.toUpperCase()}: ${vencedorDesempateAtual.jogador}`, "success");
    }

    window.confirmarGanhadorDesempate = function() {
        if(!vencedorDesempateAtual) return;

        const criterioTexto = document.getElementById('select-criterio-desempate').value === 'maior' ? 'Maior Pedra' : 'Menor Pedra';
        const resumoDesempate = `Venceu desempate por ${criterioTexto} (Pedra Sorteada: ${vencedorDesempateAtual.pedraDesempate})`;

        confirmarVencedor(vencedorDesempateAtual, resumoDesempate);
        
        desempateLista.forEach(item => {
            if(item.id !== vencedorDesempateAtual.id) {
                remove(ref(db, `bingo/alertas/${item.id}`));
            }
        });

        document.getElementById('desempate-modal').classList.remove('active');
    }

    function limparAlertasBingo() {
        remove(ref(db, 'bingo/alertas'));
        remove(ref(db, 'bingo/vencedores'));
        showToast("Alertas e vencedores limpos.", "info");
    }

    onValue(ref(db, `bingo/pedidos/${meuJogadorId}`), (snapshot) => {
        const pedido = snapshot.val();
        if(pedido && document.getElementById('tela-jogador').classList.contains('active')) {
            if(pedido.status === 'aprovado') {
                pedido.cartelas.forEach(c => minhasCartelasCompradas.push(c));
                atualizarAreaDeJogo();
                mudarModoJogador('jogo');
                showToast("✅ Pagamento Confirmado! Cartelas liberadas.", "success");
                
                gerarLojaDeCartelas(); 
                cartelasSelecionadas = [];
                document.getElementById('qtd-selecionadas').innerText = "0";
                document.getElementById('total-preco-selecionado').innerText = "R$ 0,00";
                document.getElementById('btn-confirmar-compra').style.display = 'flex';
                
                remove(ref(db, `bingo/pedidos/${meuJogadorId}`));
            } 
            else if(pedido.status === 'rejeitado') {
                showToast("❌ Seu pedido foi rejeitado. Confira o pagamento com o Admin.", "error");
                gerarLojaDeCartelas(); 
                cartelasSelecionadas = [];
                document.getElementById('qtd-selecionadas').innerText = "0";
                document.getElementById('total-preco-selecionado').innerText = "R$ 0,00";
                document.getElementById('btn-confirmar-compra').style.display = 'flex';
                
                remove(ref(db, `bingo/pedidos/${meuJogadorId}`));
            }
        }
    });

    onValue(ref(db, 'bingo/pedidos'), (snapshot) => {
        const container = document.getElementById('lista-pedidos-admin');
        const pedidos = snapshot.val();
        
        if(!pedidos || document.getElementById('tela-jogador').classList.contains('active')) {
            if(!pedidos && document.getElementById('tela-admin').classList.contains('active')) {
                container.innerHTML = '<p style="color: var(--text-muted); margin: 0;">Nenhum pedido aguardando aprovação no momento.</p>';
            }
            return;
        }

        let temPendente = false;
        let html = '';
        for(const [id, p] of Object.entries(pedidos)) {
            if(p.status === 'pendente') {
                temPendente = true;
                html += `
                <div class="pedido-card">
                    <div>
                        <strong><i class="fa-solid fa-user"></i> ${p.nome}</strong> 
                        <span style="margin-left: 10px; color: var(--text-muted); font-size: 14px;">${p.cartelas.length} cartelas - <strong style="color: var(--primary);">R$ ${p.total.toFixed(2).replace('.', ',')}</strong></span>
                    </div>
                    <div style="display:flex; gap: 8px;">
                        <button class="outline" style="border-color: var(--danger); color: var(--danger); margin:0; padding: 8px 12px;" onclick="resolverPedido('${id}', 'rejeitado')"><i class="fa-solid fa-xmark"></i> Rejeitar</button>
                        <button class="success" style="margin:0; padding: 8px 12px;" onclick="resolverPedido('${id}', 'aprovado')"><i class="fa-solid fa-check"></i> Aprovar Pagamento</button>
                    </div>
                </div>`;
            }
        }
        if(!temPendente) {
            container.innerHTML = '<p style="color: var(--text-muted); margin: 0;">Nenhum pedido aguardando aprovação no momento.</p>';
        } else {
            container.innerHTML = html;
        }
    });

    onValue(ref(db, 'bingo/config'), (snapshot) => {
        const config = snapshot.val();
        if(config) {
            document.getElementById('admin-p1').value = config.p1 || '';
            document.getElementById('admin-p2').value = config.p2 || '';
            document.getElementById('admin-p3').value = config.p3 || '';
            document.getElementById('admin-p4').value = config.p4 || '';
            document.getElementById('admin-etapa-ativa').value = config.etapaAtiva || '1';

            document.getElementById('admin-valor-cartela').value = config.valorCartela ? config.valorCartela.toFixed(2).replace(',', ',') : '10,00';
            document.getElementById('admin-pix').value = config.pix || '';

            document.getElementById('p-val-1').innerText = config.p1 || '-';
            document.getElementById('p-val-2').innerText = config.p2 || '-';
            document.getElementById('p-val-3').innerText = config.p3 || '-';
            document.getElementById('p-val-4').innerText = config.p4 || '-';

            const rodadaAtual = config.rodadaAtual || 1;
            document.querySelectorAll('.display-rodada-texto').forEach(el => el.innerText = rodadaAtual);

            for(let i=1; i<=4; i++) {
                const box = document.getElementById(`p-box-${i}`);
                if(config.etapaAtiva == i) {
                    box.classList.add('ativo');
                } else {
                    box.classList.remove('ativo');
                }
            }

            valorUnitarioCartela = config.valorCartela || 10.00;
            document.getElementById('player-valor-cartela-info').innerText = `Valor por cartela: R$ ${valorUnitarioCartela.toFixed(2).replace('.', ',')}`;
            document.getElementById('player-pix').innerText = config.pix || "";
        }
    });

    onValue(ref(db, 'bingo/estado'), (snapshot) => {
        const estado = snapshot.val();
        if(estado) {
            bolasSorteadas = estado.bolasSorteadas || [];
            bolasDisponiveis = estado.bolasDisponiveis || Array.from({length: 75}, (_, i) => i + 1);
            const bolaPendente = estado.bolaPendente;

            const painelLiberacao = document.getElementById('painel-liberacao');
            const adminPendenteTexto = document.getElementById('bola-pendente-admin');
            if(painelLiberacao && adminPendenteTexto) {
                if(bolaPendente) {
                    painelLiberacao.style.display = 'block';
                    adminPendenteTexto.innerText = formatarBola(bolaPendente);
                } else {
                    painelLiberacao.style.display = 'none';
                    adminPendenteTexto.innerText = '--';
                }
            }

            const bolaTextFormatada = bolasSorteadas.length > 0 ? formatarBola(bolasSorteadas[bolasSorteadas.length - 1]) : '--';

            document.getElementById('bola-atual').innerText = bolaTextFormatada;
            document.getElementById('qtd-sorteadas').innerText = bolasSorteadas.length;
            
            const listaAdmin = document.getElementById('lista-bolas-admin');
            listaAdmin.innerHTML = '';
            bolasSorteadas.slice().reverse().forEach((b, i) => {
                const extra = i === 0 ? "background: var(--warning); color: #000; transform: scale(1.1); border-color: #f59e0b;" : "";
                listaAdmin.innerHTML += `<div class="bola" style="${extra}">${formatarBola(b).replace(' - ', '')}</div>`;
            });

            const currentText = document.getElementById('player-bola-atual').innerText;
            if(bolasSorteadas.length > 0) {
                if(currentText !== bolaTextFormatada && currentText !== '--' && document.getElementById('modo-jogo').style.display !== 'none') {
                    showToast(`Nova Pedra Liberada: ${bolaTextFormatada}`, "success");
                }
                document.getElementById('player-bola-atual').innerText = bolaTextFormatada;
                const listaPlayer = document.getElementById('lista-bolas-player');
                listaPlayer.innerHTML = '';
                bolasSorteadas.slice().reverse().forEach((b, i) => {
                    const extra = i === 0 ? "background: var(--warning); color: #000; border-color: #f59e0b;" : "";
                    listaPlayer.innerHTML += `<div class="bola" style="${extra}">${formatarBola(b).replace(' - ', '')}</div>`;
                });
            } else {
                document.getElementById('player-bola-atual').innerText = '--';
                document.getElementById('lista-bolas-player').innerHTML = '';
            }
            
            document.querySelectorAll('#minhas-cartelas-area .num-interativo').forEach(cell => {
                const num = parseInt(cell.childNodes[0].nodeValue);
                if(bolasSorteadas.includes(num)) {
                    cell.classList.add('bola-chamada');
                } else {
                    cell.classList.remove('bola-chamada');
                }
            });
        }
    });

    onValue(ref(db, 'bingo/alertas'), (snapshot) => {
        const alertas = snapshot.val();
        const adminArea = document.getElementById('admin-conferencia-area');
        const bannerAdmin = document.getElementById('banner-alerta-bingo');
        const listaAdmin = document.getElementById('lista-alertas-admin');
        const contadorAlertas = document.getElementById('qtd-alertas-pendentes');

        if(alertas) {
            const chaves = Object.keys(alertas);
            contadorAlertas.innerText = chaves.length;
            
            if(document.getElementById('tela-admin').classList.contains('active')) {
                adminArea.style.display = 'block';
                bannerAdmin.style.display = 'block';
                
                let html = '';
                chaves.forEach(key => {
                    const alt = alertas[key];
                    const horaGrito = new Date(alt.tempoGrito).toLocaleTimeString();
                    html += `
                    <div class="alerta-item-admin">
                        <div>
                            <strong style="font-size: 16px;"><i class="fa-solid fa-user-check"></i> ${alt.jogador}</strong> gritou <span style="color: var(--danger);">${alt.tipo}</span><br>
                            <span style="font-size: 13px; color: var(--text-muted);">Pedra no grito: <strong>${formatarBola(alt.pedra)}</strong> | Às ${horaGrito}</span>
                        </div>
                        <button class="warning" style="width: auto; margin: 0; padding: 10px 15px;" onclick="abrirConferenciaJogador('${alt.id}')">
                            <i class="fa-solid fa-magnifying-glass"></i> Conferir Cartela
                        </button>
                    </div>`;
                });
                listaAdmin.innerHTML = html;
            }

            if(document.getElementById('tela-jogador').classList.contains('active')) {
                document.getElementById('banner-alerta-bingo-player').style.display = 'block';
                document.getElementById('texto-alerta-player').innerText = `HÁ ${chaves.length} JOGADOR(ES) AGUARDANDO CONFERÊNCIA DE BINGO!`;
            }

        } else {
            adminArea.style.display = 'none';
            bannerAdmin.style.display = 'none';
            document.getElementById('banner-alerta-bingo-player').style.display = 'none';
        }
    });

    onValue(ref(db, 'bingo/vencedores'), (snapshot) => {
        const vencedores = snapshot.val();
        const modalVencedor = document.getElementById('vencedor-modal');
        const listaVencedoresModal = document.getElementById('lista-vencedores-modal');

        if(vencedores) {
            const chaves = Object.keys(vencedores);
            let html = '';

            chaves.forEach(key => {
                const v = vencedores[key];
                const horaConf = new Date(v.tempoConfirmacao).toLocaleTimeString();
                const detalheDesempateHtml = v.detalhesDesempate ? `<div style="color: var(--primary); font-size: 12px; margin-top: 4px; font-weight: bold;"><i class="fa-solid fa-dice-three"></i> ${v.detalhesDesempate}</div>` : '';

                let cartelasHtml = '<div style="display: flex; flex-wrap: wrap; gap: 8px; margin-top: 10px; justify-content: center;">';
                if (v.cartelas) {
                    v.cartelas.forEach(c => {
                        cartelasHtml += renderizarHtmlCartelaParaVencedor(c);
                    });
                }
                cartelasHtml += '</div>';

                html += `
                <div style="background: #fff; padding: 15px; border-radius: 8px; border: 2px solid #f59e0b; margin-bottom: 10px;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; flex-wrap: wrap; gap: 5px;">
                        <h3 style="margin: 0; color: var(--primary);"><i class="fa-solid fa-trophy" style="color: #f59e0b;"></i> ${v.jogador} (Rodada ${v.rodada || 1})</h3>
                        <span style="font-size: 14px; font-weight: 800; background: var(--success); color: white; padding: 4px 10px; border-radius: 6px;">Prêmio: ${v.premioGanho}</span>
                    </div>
                    <p style="margin: 0 0 5px 0; font-size: 13px; color: var(--text-muted);">
                        Gritou na pedra: <strong>${formatarBola(v.pedra)}</strong> | Confirmado às: <strong>${horaConf}</strong>
                    </p>
                    ${detalheDesempateHtml}
                    <div style="margin-top: 8px; font-weight: bold; font-size: 12px; color: var(--text-main);">Cartela(s) Vencedora(s) Conferida(s):</div>
                    ${cartelasHtml}
                </div>`;
            });

            listaVencedoresModal.innerHTML = html;
            modalVencedor.classList.add('active');
        } else {
            modalVencedor.classList.remove('active');
        }
    });

    function confirmarNomeLiveAuto(nome) {
        fecharModalName();
        const isHost = (roleParaLive === 'admin');
        const containerId = isHost ? 'admin-video' : 'player-video';
        const placeholderId = isHost ? 'admin-video-placeholder' : 'player-video-placeholder';
        
        document.getElementById(placeholderId).style.display = 'none';
        const configParams = isHost ? "config.startWithVideoMuted=false&config.startWithAudioMuted=false" : "config.startWithVideoMuted=true&config.startWithAudioMuted=true";
        
        document.getElementById(containerId).innerHTML = `<iframe class="video-container" src="https://meet.jit.si/${SALA_MEET}?${configParams}&interfaceConfig.SHOW_JITSI_WATERMARK=false&interfaceConfig.TOOLBAR_BUTTONS=['microphone','camera','desktop','fullscreen','chat','participants-pane','hangup']#userInfo.displayName=${encodeURIComponent(nome)}" allow="camera; microphone; fullscreen; display-capture"></iframe>`;
    }

    function prepararLive(role) { 
        roleParaLive = role; 
        if(role === 'jogador' && nomeJogadorAtual) {
            confirmarNomeLiveAuto(nomeJogadorAtual);
        } else {
            document.getElementById('name-modal').classList.add('active'); 
            setTimeout(() => document.getElementById('modal-name-input').focus(), 100);
        }
    }
    
    function fecharModalName() { 
        document.getElementById('name-modal').classList.remove('active'); 
        document.getElementById('modal-name-input').value = ''; 
    }
    
    function confirmarNomeLive() {
        const nome = document.getElementById('modal-name-input').value.trim();
        if(!nome) return showToast("Digite um nome.", "error");
        confirmarNomeLiveAuto(nome);
    }

    window.entrarComo = entrarComo; 
    window.sairParaLogin = sairParaLogin;
    window.fecharModalSenha = fecharModalSenha; 
    window.confirmarSenhaAdmin = confirmarSenhaAdmin; 
    window.copiarPix = copiarPix; 
    window.desmarcarTodasCartelas = desmarcarTodasCartelas;
    window.toggleSelecaoLoja = toggleSelecaoLoja; 
    window.enviarPedido = enviarPedido; 
    window.mudarModoJogador = mudarModoJogador; 
    window.toggleExpandirCartelasJogo = toggleExpandirCartelasJogo; 
    window.gritarVitoria = gritarVitoria;
    window.limparAlertasBingo = limparAlertasBingo; 
    window.salvarConfiguracoes = salvarConfiguracoes; 
    window.sortearBola = sortearBola; 
    window.liberarBolaParaJogadores = liberarBolaParaJogadores;
    window.resetarJogo = resetarJogo; 
    window.prepararLive = prepararLive; 
    window.fecharModalName = fecharModalName; 
    window.confirmarNomeLive = confirmarNomeLive; 
    window.resolverPedido = resolverPedido;
    window.abrirModalRegistroJogador = abrirModalRegistroJogador;
    window.fecharModalRegistroJogador = fecharModalRegistroJogador;
    window.confirmarNomeJogador = confirmarNomeJogador;
</script>

</body>
</html>
