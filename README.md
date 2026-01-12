<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grupo Dantas | Soluções em Tecnologia</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Poppins:wght@500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- RESET E VARIÁVEIS --- */
        :root {
            --primary: #0f172a; /* Azul Escuro Profundo */
            --accent: #2563eb;  /* Azul Vibrante */
            --secondary: #64748b; /* Cinza Texto */
            --light: #f8fafc;
            --white: #ffffff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--light);
            color: var(--primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3 { font-family: 'Poppins', sans-serif; }
        a { text-decoration: none; transition: 0.3s; }
        ul { list-style: none; }

        /* --- HEADER --- */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        .logo span { color: var(--accent); }

        .nav-links { display: flex; gap: 30px; }
        .nav-links a { color: var(--secondary); font-weight: 500; }
        .nav-links a:hover { color: var(--accent); }

        .btn-contact {
            background-color: var(--accent);
            color: var(--white) !important;
            padding: 10px 24px;
            border-radius: 50px;
            font-weight: 600;
        }
        .btn-contact:hover { background-color: #1d4ed8; transform: translateY(-2px); }

        /* --- HERO SECTION --- */
        .hero {
            padding: 160px 0 100px;
            text-align: center;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: var(--white);
            border-radius: 0 0 50% 50% / 40px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            color: #94a3b8;
            max-width: 700px;
            margin: 0 auto 40px;
        }

        /* --- SERVICES --- */
        .services { padding: 80px 0; }
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        .section-title h2 { font-size: 2.2rem; margin-bottom: 10px; }
        .section-title p { color: var(--secondary); }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--white);
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: 0.3s;
            text-align: center;
        }

        .card:hover { transform: translateY(-10px); }

        .icon-box {
            width: 70px;
            height: 70px;
            background: #eff6ff;
            color: var(--accent);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            border-radius: 50%;
            margin: 0 auto 20px;
        }

        .card h3 { margin-bottom: 15px; }
        .card p { color: var(--secondary); font-size: 0.95rem; }

        /* --- FEATURED APP --- */
        .showcase {
            background-color: var(--white);
            padding: 80px 0;
            margin-top: 50px;
        }

        .showcase-wrapper {
            display: flex;
            align-items: center;
            gap: 50px;
            flex-wrap: wrap;
        }

        .showcase-text { flex: 1; min-width: 300px; }
        .showcase-image { 
            flex: 1; 
            min-width: 300px; 
            background: #f1f5f9;
            height: 300px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #cbd5e1;
        }

        .tag {
            background: #dbeafe;
            color: var(--accent);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--primary);
            color: #94a3b8;
            padding: 60px 0 30px;
            margin-top: 80px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 { color: var(--white); margin-bottom: 20px; font-size: 1.2rem; }
        .footer-col ul li { margin-bottom: 10px; }
        .footer-col a { color: #94a3b8; }
        .footer-col a:hover { color: var(--white); }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #334155;
            font-size: 0.9rem;
        }

        /* --- WHATSAPP BUTTON --- */
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: 0.3s;
        }

        .whatsapp-float:hover {
            background-color: #20ba5a;
            transform: scale(1.1);
        }

        /* MOBILE RESPONSIVE */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .nav-links { display: none; } /* Simplificado para mobile */
            .whatsapp-float { bottom: 20px; right: 20px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-wrapper">
            <div class="logo">Grupo<span>Dantas</span></div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#servicos">Serviços</a></li>
                    <li><a href="#app">Produtos</a></li>
                    <li><a href="#contato" class="btn-contact">Fale Conosco</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Transformando Ideias em<br>Soluções Digitais</h1>
            <p>Somos especialistas no desenvolvimento de Aplicativos Mobile, Sites Institucionais e Softwares de Gestão sob medida para o seu negócio.</p>
            <a href="https://wa.me/55199981117451" class="btn-contact" style="font-size: 1.1rem; padding: 15px 35px;">Solicitar Orçamento</a>
        </div>
    </section>

    <section id="servicos" class="services container">
        <div class="section-title">
            <h2>Nossas Soluções</h2>
            <p>Tecnologia de ponta para impulsionar seus resultados</p>
        </div>
        
        <div class="services-grid">
            <div class="card">
                <div class="icon-box"><i class="fa-solid fa-mobile-screen"></i></div>
                <h3>Desenvolvimento de Apps</h3>
                <p>Aplicativos nativos para Android e iOS (Flutter). Transformamos sua ideia em um produto escalável e intuitivo.</p>
            </div>
            <div class="card">
                <div class="icon-box"><i class="fa-solid fa-code"></i></div>
                <h3>Softwares Sob Medida</h3>
                <p>Sistemas de gestão e automação personalizados para atender as regras de negócio específicas da sua empresa.</p>
            </div>
            <div class="card">
                <div class="icon-box"><i class="fa-solid fa-globe"></i></div>
                <h3>Sites e Landing Pages</h3>
                <p>Sites modernos, rápidos e otimizados para o Google. A porta de entrada perfeita para seus clientes.</p>
            </div>
        </div>
    </section>

    <section id="app" class="showcase">
        <div class="container showcase-wrapper">
            <div class="showcase-text">
                <span class="tag">Produto em Destaque</span>
                <h2 style="font-size: 2.5rem; margin: 20px 0;">App Minha Kitnet</h2>
                <p style="color: var(--secondary); margin-bottom: 20px;">
                    A solução completa para gestão de aluguéis e inquilinos. Controle financeiro, contratos digitais e automação de cobranças em um só lugar.
                </p>
                <ul style="margin-bottom: 30px; color: var(--primary); font-weight: 500;">
                    <li><i class="fa-solid fa-check" style="color: var(--accent); margin-right: 10px;"></i> Gestão Financeira Completa</li>
                    <li><i class="fa-solid fa-check" style="color: var(--accent); margin-right: 10px;"></i> Backup na Nuvem</li>
                    <li><i class="fa-solid fa-check" style="color: var(--accent); margin-right: 10px;"></i> Disponível para Android e iOS</li>
                </ul>
            </div>
            <div class="showcase-image">
                <i class="fa-solid fa-house-user" style="font-size: 80px; color: #cbd5e1;"></i>
            </div>
        </div>
    </section>

    <footer id="contato">
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <div class="logo" style="color: #FFF; margin-bottom: 20px;">Grupo<span>Dantas</span></div>
                    <p>Inovação e tecnologia para levar seu negócio ao próximo nível.</p>
                </div>
                
                <div class="footer-col">
                    <h4>Contato</h4>
                    <div class="contact-item">
                        <i class="fa-brands fa-whatsapp" style="color: #25d366; font-size: 20px;"></i>
                        <a href="https://wa.me/55199981117451" target="_blank">(19) 99811-1745</a>
                    </div>
                    <div class="contact-item">
                        <i class="fa-solid fa-envelope" style="color: var(--white); font-size: 18px;"></i>
                        <a href="mailto:grupodantas@gmail.com">grupodantas@gmail.com</a>
                    </div>
                </div>

                <div class="footer-col">
                    <h4>Links Rápidos</h4>
                    <ul>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#app">Minha Kitnet</a></li>
                        <li><a href="app-ads.txt">Validação AdMob</a></li> </ul>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2026 Grupo Dantas. Todos os direitos reservados.
            </div>
        </div>
    </footer>

    <a href="https://wa.me/55199981117451?text=Ol%C3%A1%2C%20gostaria%20de%20saber%20mais%20sobre%20os%20servi%C3%A7os%20do%20Grupo%20Dantas." class="whatsapp-float" target="_blank">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

</body>
</html>
