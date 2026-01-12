<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Grupo Dantas | Soluções Digitais</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Poppins:wght@500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --primary: #0f172a;
            --accent: #3b82f6;
            --accent-gradient: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            --secondary: #64748b;
            --bg: #f8fafc;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; background-color: var(--bg); color: var(--primary); overflow-x: hidden; }
        h1, h2, h3 { font-family: 'Poppins', sans-serif; }
        img { max-width: 100%; display: block; }

        header { background: rgba(255, 255, 255, 0.9); backdrop-filter: blur(10px); position: fixed; width: 100%; top: 0; z-index: 1000; box-shadow: 0 4px 20px rgba(0,0,0,0.05); }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }
        .nav-wrapper { display: flex; justify-content: space-between; align-items: center; height: 80px; }
        .logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); }
        .logo span { color: var(--accent); }
        .btn-contact { background: var(--accent-gradient); color: white; padding: 10px 24px; border-radius: 50px; text-decoration: none; font-weight: 600; }

        .hero { padding: 160px 0 100px; text-align: center; }
        .hero h1 { font-size: 3rem; margin-bottom: 20px; font-weight: 800; }
        
        .project-card { display: flex; align-items: center; gap: 60px; margin-bottom: 120px; }
        .project-card.reverse { flex-direction: row-reverse; }
        .project-info { flex: 1; }
        .tag { background: #dbeafe; color: var(--accent); padding: 6px 14px; border-radius: 20px; font-size: 0.85rem; font-weight: 700; text-transform: uppercase; margin-bottom: 20px; display: inline-block; }
        
        .mockup-container { flex: 1; display: flex; justify-content: center; perspective: 1000px; }
        .phone-frame { width: 300px; height: 600px; background: #1e293b; border-radius: 45px; padding: 12px; box-shadow: 0 30px 60px -15px rgba(0,0,0,0.3); transform: rotateY(-10deg) rotateX(5deg); transition: 0.5s; }
        .reverse .phone-frame { transform: rotateY(10deg) rotateX(5deg); }
        .phone-frame:hover { transform: rotateY(0) rotateX(0) translateY(-10px); }
        .screen { width: 100%; height: 100%; background: #000; border-radius: 35px; overflow: hidden; }
        .screen img { width: 100%; height: 100%; object-fit: cover; }

        .features li { margin-bottom: 10px; list-style: none; }
        .features i { color: var(--accent); margin-right: 10px; }

        footer { background: var(--primary); color: #94a3b8; padding: 80px 0 30px; text-align: center; }
        .whatsapp-float { position: fixed; bottom: 30px; right: 30px; width: 60px; height: 60px; background: #25d366; color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4); z-index: 999; }

        @media (max-width: 900px) {
            .project-card, .project-card.reverse { flex-direction: column; text-align: center; }
            .phone-frame { width: 260px; height: 520px; transform: none !important; }
            .hero h1 { font-size: 2.2rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-wrapper">
            <div class="logo">Grupo<span>Dantas</span></div>
            <a href="https://wa.me/55199981117451" class="btn-contact">Orçamento</a>
        </div>
    </header>

    <section class="hero">
        <div class="container" data-aos="fade-up">
            <h1>Transformamos ideias em<br><span style="color: var(--accent)">Aplicativos de Sucesso</span></h1>
            <p style="color: var(--secondary); margin-top: 20px;">Especialistas em desenvolvimento mobile (Android & iOS) e sistemas de gestão.</p>
        </div>
    </section>

    <section class="container" style="padding-bottom: 100px;">
        
        <div class="project-card" data-aos="fade-right">
            <div class="project-info">
                <span class="tag">Gestão Imobiliária</span>
                <h3>App Minha Kitnet</h3>
                <p>Plataforma completa para gestão de aluguéis. Dashboard intuitivo, controle financeiro e cálculos automáticos.</p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Dashboard Gestor</li>
                    <li><i class="fa-solid fa-check"></i> Controle Financeiro</li>
                    <li><i class="fa-solid fa-check"></i> Backup Nuvem</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7993.png" alt="Minha Kitnet Gestor">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card reverse" data-aos="fade-left">
            <div class="project-info">
                <span class="tag">Produtividade & Design</span>
                <h3>Rotação Criativa</h3>
                <p>Suite de ferramentas para criadores. Crie mockups, redimensione imagens para lojas e edite panoramas.</p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Smart Resizer (App Store)</li>
                    <li><i class="fa-solid fa-check"></i> Editor Panorama</li>
                    <li><i class="fa-solid fa-check"></i> Criador de Mockups</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7996.png" alt="App Rotação">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card" data-aos="fade-right">
            <div class="project-info">
                <span class="tag">Financeiro Avançado</span>
                <h3>Controle de Fluxo de Caixa</h3>
                <p>Visualize receitas e despesas com clareza. Gráficos detalhados e previsibilidade financeira para o seu negócio.</p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Gráficos Interativos</li>
                    <li><i class="fa-solid fa-check"></i> Relatórios Mensais</li>
                    <li><i class="fa-solid fa-check"></i> Dark Mode</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7995.png" alt="Financeiro Kitnet">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card reverse" data-aos="fade-left">
            <div class="project-info">
                <span class="tag">Fintech</span>
                <h3>Controle de Empréstimos</h3>
                <p>Gestão completa de carteira de clientes, cálculo de juros e controle de inadimplência.</p>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="crop_1242x2688_PRO.jpg" alt="Aguardando Upload" onerror="this.style.display='none'; this.parentElement.style.background='#334155'">
                    </div>
                </div>
            </div>
        </div>

    </section>

    <footer>
        <div class="container">
            <div class="logo" style="color: white; margin-bottom: 20px;">Grupo<span>Dantas</span></div>
            <p>Desenvolvendo o futuro do seu negócio.</p>
            <br>
            <a href="app-ads.txt" style="color: #475569; font-size: 0.8rem; border: 1px solid #334155; padding: 5px 10px; border-radius: 5px; text-decoration: none;">AdMob Validation</a>
            <p style="margin-top: 30px; font-size: 0.9rem; color: #475569;">&copy; 2026 Grupo Dantas.</p>
        </div>
    </footer>

    <a href="https://wa.me/+55199981117451" class="whatsapp-float" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script> AOS.init(); </script>
</body>
</html>
