<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mente Veloz - Jocivania</title>
    <style>
        :root {
            --primary-color: #6A0DAD;
            --secondary-color: #FFD700;
            --accent-color: #4C00A3;
            --light-color: #F5F5F5;
            --dark-color: #333333;
            --font-primary: 'Montserrat', sans-serif;
            --font-secondary: 'Raleway', sans-serif;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-secondary);
            color: var(--dark-color);
            line-height: 1.6;
            background-color: var(--light-color);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        
        .logo {
            font-family: var(--font-primary);
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .section {
            padding: 60px 0;
            display: none;
        }
        
        .section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        h2 {
            font-family: var(--font-primary);
            color: var(--primary-color);
            margin-bottom: 20px;
            text-align: center;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        input[type="text"],
        input[type="email"] {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        .btn {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: var(--accent-color);
        }
        
        .btn-next {
            background-color: var(--secondary-color);
            color: var(--dark-color);
        }
        
        .btn-next:hover {
            background-color: #FFC400;
        }
        
        .service-card {
            background-color: white;
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-title {
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .about-content {
            background-color: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto 20px;
            display: block;
            border: 5px solid var(--secondary-color);
        }
        
        .cta-section {
            text-align: center;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 40px 20px;
            border-radius: 8px;
        }
        
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
        }
        
        .progress-bar {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
            position: relative;
        }
        
        .progress-step {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            z-index: 2;
        }
        
        .progress-step.active {
            background-color: var(--primary-color);
            color: white;
        }
        
        .progress-bar::before {
            content: '';
            position: absolute;
            top: 15px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: #ddd;
            z-index: 1;
        }
        
        footer {
            text-align: center;
            padding: 20px 0;
            background-color: var(--dark-color);
            color: white;
            margin-top: 40px;
        }
        
        @media (min-width: 768px) {
            .services-container {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 20px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Raleway:wght@400;500&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">Mente Veloz</div>
            <div class="tagline">Transformando sonhos em realidade</div>
        </div>
    </header>
    
    <main class="container">
        <div class="progress-bar">
            <div class="progress-step active">1</div>
            <div class="progress-step">2</div>
            <div class="progress-step">3</div>
            <div class="progress-step">4</div>
        </div>
        
        <!-- Etapa 1: Nome e Email -->
        <section id="etapa1" class="section active">
            <h2>Vamos começar!</h2>
            <form id="form-contato">
                <div class="form-group">
                    <label for="nome">Seu nome completo</label>
                    <input type="text" id="nome" name="nome" required>
                </div>
                <div class="form-group">
                    <label for="email">Seu melhor email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <button type="button" class="btn btn-next" onclick="proximaEtapa(1)">Próximo</button>
            </form>
        </section>
        
        <!-- Etapa 2: Serviços -->
        <section id="etapa2" class="section">
            <h2>Como posso ajudar você?</h2>
            <p>Escolha um dos serviços abaixo para transformar seu negócio:</p>
            
            <div class="services-container">
                <div class="service-card">
                    <h3 class="service-title">Consultoria para Iniciar Negócios</h3>
                    <p>Orientação completa desde a ideia até a execução do seu negócio, com planejamento estratégico, análise de mercado e definição de metas realistas.</p>
                    <button class="btn" onclick="selecionarServico('consultoria')">Selecionar</button>
                </div>
                
                <div class="service-card">
                    <h3 class="service-title">Transformação de Atendimento ao Cliente</h3>
                    <p>Estratégias para encantar seus clientes, criar experiências memoráveis e fidelizar através de um atendimento humanizado e eficiente.</p>
                    <button class="btn" onclick="selecionarServico('atendimento')">Selecionar</button>
                </div>
            </div>
            
            <div class="navigation">
                <button class="btn" onclick="proximaEtapa(2, 'voltar')">Voltar</button>
            </div>
        </section>
        
        <!-- Etapa 3: Quem sou eu -->
        <section id="etapa3" class="section">
            <h2>Quem sou eu</h2>
            
            <div class="about-content">
                <img src="https://placehold.co/200x200/6A0DAD/FFFFFF?text=J" alt="Jocivania - Fundadora da Mente Veloz" class="profile-img">
                
                <p>Sou Jocivania, fundadora da Mente Veloz, uma empreendedora determinada e autêntica que acredita no poder da coragem e da clareza para transformar sonhos em realidade.</p>
                
                <p>Desde 2020 iniciei minha trajetória com sessões espirituais, mas minha paixão pelo empreendedorismo nasceu muito antes, ainda na adolescência. Durante anos, o medo e a vergonha me impediram de seguir esse caminho, mas hoje compreendo que para viver meus sonhos é preciso dar passos firmes e confiar no processo.</p>
                
                <p>Atualmente, estou me graduando em Administração e unindo essa formação com minha bagagem em autoconhecimento e espiritualidade. Essa combinação me permite enxergar os negócios não apenas como números, mas como projetos de vida.</p>
                
                <p>Meu propósito é ajudar pessoas a começarem seus negócios, transformar atendimento em encantamento e inspirar outros a conquistarem seus próprios sonhos.</p>
                
                <p>Diferente de abordagens tradicionais, eu uno prática administrativa, mentalidade de alta performance e desenvolvimento humano, trazendo soluções completas e humanizadas. Acredito que encantar clientes começa no cuidado genuíno com as pessoas — e é isso que me move todos os dias.</p>
            </div>
            
            <div class="navigation">
                <button class="btn" onclick="proximaEtapa(3, 'voltar')">Voltar</button>
                <button class="btn btn-next" onclick="proximaEtapa(3)">Próximo</button>
            </div>
        </section>
        
        <!-- Etapa 4: Call to Action -->
        <section id="etapa4" class="section">
            <div class="cta-section">
                <h2>Não perca essa chance!</h2>
                <p>Transforme seu sonho empreendedor em realidade com orientação especializada e suporte personalizado.</p>
                <p>Vamos juntos construir o negócio que você sempre imaginou!</p>
                
                <div id="resumo-escolha">
                    <!-- Aqui será exibido o resumo da escolha -->
                </div>
                
                <button class="btn" style="margin-top: 20px; background-color: var(--secondary-color); color: var(--dark-color);" onclick="finalizarPedido()">Solicitar Contato</button>
            </div>
            
            <div class="navigation">
                <button class="btn" onclick="proximaEtapa(4, 'voltar')">Voltar</button>
            </div>
        </section>
    </main>
    
    <footer>
        <div class="container">
            <p>Mente Veloz - &copy; 2023 - Todos os direitos reservados</p>
        </div>
    </footer>

    <script>
        let dadosCliente = {
            nome: '',
            email: '',
            servico: ''
        };
        
        let etapaAtual = 1;
        
        function atualizarProgresso(etapa) {
            const steps = document.querySelectorAll('.progress-step');
            steps.forEach((step, index) => {
                if (index + 1 <= etapa) {
                    step.classList.add('active');
                } else {
                    step.classList.remove('active');
                }
            });
        }
        
        function proximaEtapa(etapa, direcao = 'avancar') {
            if (direcao === 'avancar') {
                // Validar etapa atual antes de avançar
                if (etapa === 1) {
                    const nome = document.getElementById('nome').value;
                    const email = document.getElementById('email').value;
                    
                    if (!nome || !email) {
                        alert('Por favor, preencha todos os campos.');
                        return;
                    }
                    
                    dadosCliente.nome = nome;
                    dadosCliente.email = email;
                } else if (etapa === 2 && !dadosCliente.servico) {
                    alert('Por favor, selecione um serviço.');
                    return;
                }
                
                etapaAtual = etapa + 1;
            } else {
                etapaAtual = etapa - 1;
            }
            
            // Esconder todas as seções e mostrar apenas a atual
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            
            document.getElementById('etapa' + etapaAtual).classList.add('active');
            atualizarProgresso(etapaAtual);
            
            // Rolar para o topo
            window.scrollTo(0, 0);
            
            // Se for a última etapa, atualizar o resumo
            if (etapaAtual === 4) {
                atualizarResumo();
            }
        }
        
        function selecionarServico(servico) {
            dadosCliente.servico = servico;
            
            // Destacar visualmente o serviço selecionado
            document.querySelectorAll('.service-card').forEach(card => {
                card.style.border = 'none';
            });
            
            // Avançar para a próxima etapa após 500ms
            setTimeout(() => {
                proximaEtapa(2);
            }, 500);
        }
        
        function atualizarResumo() {
            const resumo = document.getElementById('resumo-escolha');
            let nomeServico = '';
            
            if (dadosCliente.servico === 'consultoria') {
                nomeServico = 'Consultoria para Iniciar Negócios';
            } else if (dadosCliente.servico === 'atendimento') {
                nomeServico = 'Transformação de Atendimento ao Cliente';
            }
            
            resumo.innerHTML = `
                <p><strong>Nome:</strong> ${dadosCliente.nome}</p>
                <p><strong>Email:</strong> ${dadosCliente.email}</p>
                <p><strong>Serviço escolhido:</strong> ${nomeServico}</p>
            `;
        }
        
        function finalizarPedido() {
            alert(`Obrigada, ${dadosCliente.nome}! Entrarei em contato em breve pelo email ${dadosCliente.email} para conversarmos sobre ${dadosCliente.servico === 'consultoria' ? 'sua consultoria para iniciar negócios' : 'a transformação do seu atendimento ao cliente'}.`);
            // Aqui você normalmente enviaria os dados para um backend
        }
    </script>
</body>
</html>
