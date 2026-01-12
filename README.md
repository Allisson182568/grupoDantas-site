<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Grupo Dantas | Desenvolvimento de Software Premium</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Poppins:wght@500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        /* --- RESET E VARIÁVEIS --- */
        :root {
            --primary: #0f172a;
            --primary-light: #1e293b;
            --accent: #3b82f6; /* Azul mais brilhante */
            --accent-gradient: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            --secondary: #64748b;
            --light: #f8fafc;
            --white: #ffffff;
            --shadow: 0 20px 40px rgba(0,0,0,0.08);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--light);
            color: var(--primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 { font-family: 'Poppins', sans-serif; }
        a { text-decoration: none; transition: 0.3s; }
        ul { list-style: none; }

        /* --- GRADIENT TEXT --- */
        .text-gradient {
            background: var(--accent-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: inline-block;
        }

        /* --- HEADER --- */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 15px rgba(0,0,0,0.03);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: 0.3s;
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
            font-size: 1.7rem;
            font-weight: 800;
            color: var(--primary);
            letter-spacing: -0.5px;
        }
        .logo span { color: var(--accent); }

        .nav-links { display: flex; gap: 35px; align-items: center; }
        .nav-links a { color: var(--primary); font-weight: 600; font-size: 0.95rem; }
        .nav-links a:hover { color: var(--accent); }

        .btn-contact {
            background: var(--accent-gradient);
            color: var(--white) !important;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 600;
            box-shadow: 0 10px 20px -10px rgba(37, 99, 235, 0.5);
        }
        .btn-contact:hover { transform: translateY(-3px); box-shadow: 0 15px 30px -10px rgba(37, 99, 235, 0.6); }

        /* --- HERO SECTION --- */
        .hero {
            padding: 180px 0 120px;
            text-align: center;
            background-color: var(--primary);
            background-image: radial-gradient(circle at top right, rgba(59, 130, 246, 0.15), transparent 40%),
                              radial-gradient(circle at bottom left, rgba(37, 99, 235, 0.1), transparent 40%);
            color: var(--white);
            position: relative;
            overflow: hidden;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 25px;
            line-height: 1.15;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.25rem;
            color: #cbd5e1;
            max-width: 750px;
            margin: 0 auto 45px;
        }

        /* --- SERVICES --- */
        .section-padding { padding: 100px 0; }
        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }
        .section-title h2 { font-size: 2.5rem; margin-bottom: 15px; font-weight: 700; }
        .section-title p { color: var(--secondary); font-size: 1.1rem; max-width: 600px; margin: 0 auto; }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 35px;
        }

        .card {
            background: var(--white);
            padding: 50px 40px;
            border-radius: 24px;
            box-shadow: var(--shadow);
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            text-align: left;
            border: 1px solid #f1f5f9;
            height: 100%;
        }

        .card:hover { transform: translateY(-12px); border-color: #dbeafe; }

        .icon-box {
            width: 65px;
            height: 65px;
            background: var(--accent-gradient);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 26px;
            border-radius: 18px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px -5px rgba(37, 99, 235, 0.3);
        }

        .card h3 { margin-bottom: 15px; font-size: 1.35rem; }
        .card p { color: var(--secondary); font-size: 1rem; line-height: 1.7; }

        /* --- PORTFOLIO SECTION --- */
        .portfolio {
            background-color: #f1f5f9;
            position: relative;
        }
        
        .project-card {
            display: flex;
            align-items: center;
            gap: 60px;
            margin-bottom: 100px;
        }
        .project-card.reverse { flex-direction: row-reverse; }

        .project-info { flex: 1; }
        .project-tag {
            display: inline-block;
            background: #dbeafe;
            color: var(--accent);
            padding: 6px 14px;
            border-radius: 30px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            margin-bottom: 20px;
            letter-spacing: 0.5px;
        }
        .project-info h3 { font-size: 2.2rem; margin-bottom: 20px; }
        .project-info p { color: var(--secondary); font-size: 1.05rem; margin-bottom: 30px; }
        
        .feature-list li {
            margin-bottom: 12px;
            font-weight: 500;
            display: flex;
            align-items: center;
        }
        .feature-list i { color: var(--accent); margin-right: 12px; background: #dbeafe; padding: 5px; border-radius: 50%; font-size: 0.8rem; }

        .project-mockup {
            flex: 1;
            position: relative;
            display: flex;
            justify-content: center;
            perspective: 1000px;
        }
        
        /* Mockup de Celular Genérico */
        .phone-frame {
            width: 300px;
            height: 600px;
            background: var(--primary);
            border-radius: 40px;
            padding: 10px;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25);
            position: relative;
            transform: rotateY(-5deg) rotateX(2deg);
            transition: 0.5s;
        }
        .phone-frame:hover { transform: rotateY(0deg) rotateX(0deg) translateY(-10px); }

        .phone-screen {
            width: 100%;
            height: 100%;
            background: #000;
            border-radius: 32px;
            overflow: hidden;
            position: relative;
        }
        
        .phone-screen img, .phone-screen video {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Garante que a imagem preencha a tela */
        }

        /* Placeholder para quando não tiver imagem/gif */
        .gif-placeholder {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: linear-gradient(45deg, #1e293b, #0f172a);
            color: #64748b;
            text-align: center;
            padding: 20px;
        }
        .gif-placeholder i { font-size: 50px; margin-bottom: 20px; opacity: 0.5; }

        /* --- FOOTER --- */
        footer {
            background-color: var(--primary);
            color: #94a3b8;
            padding: 80px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr;
            gap: 50px;
            margin-bottom: 60px;
        }

        .footer-col p { margin-top: 20px; max-width: 300px; }
        .footer-col h4 { color: var(--white); margin-bottom: 25px; font-size: 1.1rem; }
        .footer-col ul li { margin-bottom: 15px; }
        .footer-col a { color: #94a3b8; transition: 0.2s; }
        .footer-col a:hover { color: var(--white); }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 18px;
        }
        .contact-link i { font-size: 1.2rem; color: var(--accent); }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #1e293b;
            font-size: 0.9rem;
            color: #64748b;
        }

        /* --- WHATSAPP BUTTON --- */
        .whatsapp-float {
            position: fixed;
            width: 65px;
            height: 65px;
            bottom: 40px;
            right: 40px;
            background: linear-gradient(45deg, #25d366, #128c7e);
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 32px;
            box-shadow: 0 10px 20px -5px rgba(37, 211, 102, 0.4);
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: 0.3s;
        }

        .whatsapp-float:hover { transform: scale(1.1) translateY(-5px); }

        /* MOBILE RESPONSIVE */
        @media (max-width: 992px) {
            .hero h1 { font-size: 2.8rem; }
            .project-card, .project-card.reverse { flex-direction: column; gap: 40px; text-align: center; }
            .project-info h3 { font-size: 1.8rem; }
            .feature-list { display: inline-block; text-align: left; }
            .phone-frame { width: 260px; height: 520px; margin: 0 auto; transform: none; }
            .phone-frame:hover { transform: none; }
            .footer-grid { grid-template-columns: 1fr; gap: 40px; }
        }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero { padding: 140px 0 80px; border-radius: 0 0 30px 30px; }
            .hero h1 { font-size: 2.2rem; }
            .whatsapp-float { bottom: 25px; right: 25px; width: 55px; height: 55px; font-size: 28px; }
            .card { padding: 35px 25px; }
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
                    <li><a href="#portfolio">Portfólio</a></li>
                    <li><a href="#contato" class="btn-contact">Solicitar Orçamento</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container" data-aos="fade-up">
            <h1>Nós criamos o software que<br> <span class="text-gradient">impulsiona o seu negócio</span></h1>
            <p>Especialistas em desenvolvimento mobile e web. Transformamos desafios complexos em soluções digitais intuitivas, escaláveis e de alto impacto.</p>
            <a href="https://wa.me/55199981117451" class="btn-contact" style="font-size: 1.1rem; padding: 15px 38px;">Iniciar Projeto</a>
        </div>
    </section>

    <section id="servicos" class="section-padding container">
        <div class="section-title" data-aos="fade-up">
            <h2><span class="text-gradient">Nossas Expertises</span></h2>
            <p>Combinamos design estratégico e engenharia de software robusta para entregar resultados excepcionais.</p>
        </div>
        
        <div class="services-grid">
            <div class="card" data-aos="fade-up" data-aos-delay="100">
                <div class="icon-box"><i class="fa-solid fa-mobile-screen-button"></i></div>
                <h3>Desenvolvimento Mobile</h3>
                <p>Apps nativos de alta performance para iOS e Android usando Flutter. Foco em experiência do usuário fluida e design moderno.</p>
            </div>
            <div class="card" data-aos="fade-up" data-aos-delay="200">
                <div class="icon-box"><i class="fa-solid fa-code-branch"></i></div>
                <h3>Sistemas Sob Medida</h3>
                <p>Softwares corporativos, CRMs e ERPs personalizados. Automatize processos e ganhe eficiência operacional com soluções feitas para você.</p>
            </div>
            <div class="card" data-aos="fade-up" data-aos-delay="300">
                <div class="icon-box"><i class="fa-solid fa-laptop-code"></i></div>
                <h3>Plataformas Web</h3>
                <p>Sites institucionais, portais e dashboards interativos. Rápidos, seguros e otimizados para converter visitantes em clientes.</p>
            </div>
        </div>
    </section>

    <section id="portfolio" class="section-padding portfolio">
        <div class="container">
            <div class="section-title" data-aos="fade-up">
                <h2><span class="text-gradient">Cases de Sucesso</span></h2>
                <p>Conheça alguns dos projetos que desenvolvemos e o impacto que geraram.</p>
            </div>

            <div class="project-card" data-aos="fade-right">
                <div class="project-info">
                    <span class="project-tag">Gestão Imobiliária</span>
                    <h3>App Minha Kitnet</h3>
                    <p>Uma solução completa e intuitiva para proprietários e gestores de aluguéis. Simplifica o controle financeiro, a gestão de contratos e a comunicação com inquilinos.</p>
                    <ul class="feature-list">
                        <li><i class="fa-solid fa-check"></i> Dashboard financeiro com gráficos claros</li>
                        <li><i class="fa-solid fa-check"></i> Gestão de inquilinos e propriedades</li>
                        <li><i class="fa-solid fa-check"></i> Backup automático na nuvem (Firebase)</li>
                        <li><i class="fa-solid fa-check"></i> Interface limpa e fácil de usar</li>
                    </ul>
                </div>
                <div class="project-mockup">
                    <div class="phone-frame">
                        <div class="phone-screen">
                            <img src="crop_1242x2688_PRO.jpg" alt="Tela do App Minha Kitnet">
                        </div>
                    </div>
                </div>
            </div>

            <div class="project-card reverse" data-aos="fade-left">
                <div class="project-info">
                    <span class="project-tag">Fintech / Gestão</span>
                    <h3>Controle de Empréstimos</h3>
                    <p>Sistema robusto para gerenciamento de carteiras de empréstimos. Oferece controle total sobre parcelas, juros, vencimentos e status de pagamento dos clientes.</p>
                    <ul class="feature-list">
                        <li><i class="fa-solid fa-check"></i> Cálculo automático de juros e multas</li>
                        <li><i class="fa-solid fa-check"></i> Relatórios de inadimplência</li>
                        <li><i class="fa-solid fa-check"></i> Notificações de cobrança</li>
                        <li><i class="fa-solid fa-check"></i> Histórico completo do cliente</li>
                    </ul>
                </div>
                <div class="project-mockup">
                    <div class="phone-frame">
                        <div class="phone-screen">
                            <div class="gif-placeholder">
                                <i class="fa-solid fa-hand-holding-dollar"></i>
                                <p>GIF do App de<br>Empréstimos Aqui</p>
                            </div>
                            </div>
                    </div>
                </div>
            </div>

            <div class="project-card" data-aos="fade-right">
                <div class="project-info">
                    <span class="project-tag">Marketing Digital / AdTech</span>
                    <h3>Plataforma Rotação</h3>
                    <p>Solução inovadora para gestão e divulgação de mídia digital rotativa. Conecta anunciantes a espaços publicitários de forma dinâmica e mensurável.</p>
                    <ul class="feature-list">
                        <li><i class="fa-solid fa-check"></i> Agendamento de campanhas</li>
                        <li><i class="fa-solid fa-check"></i> Segmentação de público-alvo</li>
                        <li><i class="fa-solid fa-check"></i> Analytics de desempenho em tempo real</li>
                        <li><i class="fa-solid fa-check"></i> Integração com displays digitais</li>
                    </ul>
                </div>
                <div class="project-mockup">
                    <div class="phone-frame">
                        <div class="phone-screen">
                            <div class="gif-placeholder" style="background: linear-gradient(45deg, #3b82f6, #1e293b);">
                                <i class="fa-solid fa-bullseye" style="color: white;"></i>
                                <p style="color: white;">GIF da Plataforma<br>Rotação Aqui</p>
                            </div>
                             </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <footer id="contato">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="logo" style="color: #FFF;">Grupo<span>Dantas</span></div>
                    <p>Parceiro estratégico em tecnologia, focado em entregar soluções de software que geram valor real para o seu negócio.</p>
                </div>
                
                <div class="footer-col">
                    <h4>Fale Conosco</h4>
                    <div class="contact-link">
                        <i class="fa-brands fa-whatsapp"></i>
                        <a href="https://wa.me/55199981117451" target="_blank">(19) 99811-1745</a>
                    </div>
                    <div class="contact-link">
                        <i class="fa-solid fa-envelope"></i>
                        <a href="mailto:grupodantas@gmail.com">grupodantas@gmail.com</a>
                    </div>
                    <div class="contact-link" style="margin-top: 25px;">
                        <a href="app-ads.txt" style="display: flex; align-items: center; gap: 10px; background: rgba(255,255,255,0.05); padding: 8px 15px; border-radius: 8px;">
                            <i class="fa-solid fa-file-code" style="font-size: 1rem;"></i>
                            <span style="font-size: 0.9rem;">Validação AdMob (app-ads.txt)</span>
                        </a>
                    </div>
                </div>

                <div class="footer-col">
                    <h4>Navegação</h4>
                    <ul>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#portfolio">Portfólio</a></li>
                        <li><a href="#contato">Contato</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2026 Grupo Dantas Soluções Digitais. Todos os direitos reservados.
            </div>
        </div>
    </footer>

    <a href="https://wa.me/55199981117451?text=Ol%C3%A1%2C%20vim%20pelo%20site%20e%20gostaria%20de%20falar%20sobre%20um%20projeto%20de%20software." class="whatsapp-float" target="_blank" aria-label="Contato via WhatsApp">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({
            duration: 800, // Duração da animação em ms
            once: true, // Anima apenas uma vez ao rolar
            offset: 100 // Começa a animar 100px antes do elemento aparecer
        });
    </script>

</body>
</html>
