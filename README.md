


<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Grupo Dantas | Soluções Digitais</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Poppins:wght@500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        /* --- CONFIGURAÇÕES GERAIS --- */
        :root {
            --primary: #0f172a;
            --accent: #3b82f6;
            --accent-gradient: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            --secondary: #64748b;
            --bg: #f8fafc;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        html {
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        body { 
            font-family: 'Inter', sans-serif; 
            background-color: var(--bg); 
            color: var(--primary); 
            overflow-x: hidden; 
        }

        h1, h2, h3 { font-family: 'Poppins', sans-serif; }
        img { max-width: 100%; display: block; }

        /* --- HEADER --- */
        header { 
            background: rgba(255, 255, 255, 0.95); 
            backdrop-filter: blur(10px); 
            position: fixed; 
            width: 100%; 
            top: 0; 
            z-index: 1000; 
            box-shadow: 0 4px 20px rgba(0,0,0,0.05); 
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
            transition: height 0.3s;
        }

        .logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); }
        .logo span { color: var(--accent); }
        
        .btn-contact { 
            background: var(--accent-gradient); 
            color: white; 
            padding: 10px 24px; 
            border-radius: 50px; 
            text-decoration: none; 
            font-weight: 600; 
            transition: transform 0.2s;
            font-size: 0.95rem;
        }
        .btn-contact:active { transform: scale(0.95); }

        /* --- HERO SECTION --- */
        .hero { 
            padding: 160px 0 100px; 
            text-align: center; 
        }
        
        .hero h1 { 
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 20px; 
            font-weight: 800; 
            line-height: 1.2;
        }

        /* --- PROJECT CARDS --- */
        .project-card { 
            display: flex; 
            align-items: center; 
            gap: 60px; 
            margin-bottom: 120px; 
        }
        
        .project-card.reverse { flex-direction: row-reverse; }
        .project-info { flex: 1; }
        
        .tag { 
            background: #dbeafe; 
            color: var(--accent); 
            padding: 6px 14px; 
            border-radius: 20px; 
            font-size: 0.85rem; 
            font-weight: 700; 
            text-transform: uppercase; 
            margin-bottom: 20px; 
            display: inline-block; 
        }

        /* --- MOCKUP (CELULAR) --- */
        .mockup-container { 
            flex: 1; 
            display: flex; 
            justify-content: center; 
            perspective: 1000px; 
        }
        
        .phone-frame { 
            width: 300px; 
            height: 600px; 
            background: #1e293b; 
            border-radius: 45px; 
            padding: 12px; 
            box-shadow: 0 30px 60px -15px rgba(0,0,0,0.3); 
            transform: rotateY(-10deg) rotateX(5deg); 
            transition: 0.5s; 
            position: relative;
        }
        
        .reverse .phone-frame { transform: rotateY(10deg) rotateX(5deg); }
        .phone-frame:hover { transform: rotateY(0) rotateX(0) translateY(-10px); }
        
        .screen { 
            width: 100%; 
            height: 100%; 
            background: #000; 
            border-radius: 35px; 
            overflow: hidden; 
        }
        
        .screen img { 
            width: 100%; 
            height: 100%; 
            object-fit: cover; 
        }

        .features li { margin-bottom: 10px; list-style: none; font-weight: 500; }
        .features i { color: var(--accent); margin-right: 10px; }

        /* --- LEGAL SECTION --- */
        .legal-section { background: white; padding: 80px 0; border-top: 1px solid #e2e8f0; }
        .legal-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-top: 40px; }
        .legal-card { background: var(--bg); padding: 30px; border-radius: 16px; text-align: center; transition: 0.3s; border: 1px solid #e2e8f0; display: block; color: var(--primary); text-decoration: none; }
        .legal-card:hover { transform: translateY(-5px); border-color: var(--accent); box-shadow: 0 10px 30px rgba(59, 130, 246, 0.1); }
        .legal-card i { font-size: 2rem; color: var(--accent); margin-bottom: 15px; }
        .legal-card h4 { margin-bottom: 10px; font-size: 1.1rem; }
        .legal-card p { font-size: 0.9rem; color: var(--secondary); }

        /* --- FOOTER --- */
        footer { background: var(--primary); color: #94a3b8; padding: 80px 0 30px; text-align: center; }
        .whatsapp-float { position: fixed; bottom: 30px; right: 30px; width: 60px; height: 60px; background: #25d366; color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4); z-index: 999; transition: transform 0.2s; }
        .whatsapp-float:hover { transform: scale(1.1); }

        /* --- RESPONSIVIDADE (TABLET E CELULAR) --- */
        @media (max-width: 900px) {
            .nav-wrapper { height: 70px; }
            .hero { padding: 140px 0 60px; }
            
            .project-card, .project-card.reverse { 
                flex-direction: column; 
                text-align: center; 
                gap: 40px; 
                margin-bottom: 80px;
            }

            .features { 
                display: inline-block; 
                text-align: left; 
                margin-top: 20px; 
            }

            /* Remove o efeito 3D no celular para evitar bugs */
            .phone-frame, .reverse .phone-frame { 
                transform: none !important; 
                margin: 0 auto;
            }
            .phone-frame:hover { transform: none !important; }
        }

        /* --- RESPONSIVIDADE (CELULARES PEQUENOS) --- */
        @media (max-width: 480px) {
            .logo { font-size: 1.2rem; }
            .btn-contact { padding: 8px 16px; font-size: 0.85rem; }
            
            .hero h1 { font-size: 2.2rem; } 
            
            .phone-frame { 
                width: 260px; 
                height: 520px; 
                border-radius: 35px;
            }

            .whatsapp-float { width: 50px; height: 50px; font-size: 24px; bottom: 20px; right: 20px; }
            
            .legal-section { padding: 50px 0; }
            .legal-grid { grid-template-columns: 1fr; } 
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-wrapper">
            <div class="logo">Grupo<span>Dantas</span></div>
            <a href="https://wa.me/5519981117451" class="btn-contact">Orçamento</a>
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
                <span class="tag">Ferramenta Dev</span>
                <h3>Smart Resizer</h3>
                <p>Ajuste automático de screenshots para os padrões exigidos pela App Store e Google Play.</p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Iphone 6.5" e 5.5"</li>
                    <li><i class="fa-solid fa-check"></i> Padronização Automática</li>
                    <li><i class="fa-solid fa-check"></i> Exportação Rápida</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7997.png" alt="Smart Resizer">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card reverse" data-aos="fade-left">
            <div class="project-info">
                <span class="tag">Financeiro Avançado</span>
                <h3>Controle de Fluxo de Caixa</h3>
                <p>Visualize receitas e despesas com clareza. Gráficos detalhados e previsibilidade financeira.</p>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7995.png" alt="Financeiro Kitnet">
                    </div>
                </div>
            </div>
        </div>

    </section>

    <section class="legal-section">
        <div class="container">
            <div style="text-align: center; max-width: 600px; margin: 0 auto;">
                <h2 style="font-size: 2rem; margin-bottom: 10px;">Transparência e Segurança</h2>
                <p style="color: var(--secondary);">Nossa conformidade com as diretrizes da Apple (App Store) e Google (Play Store).</p>
            </div>

            <div class="legal-grid">
                <a href="politica.html" class="legal-card">
                    <i class="fa-solid fa-shield-halved"></i>
                    <h4>Política de Privacidade</h4>
                    <p>Como coletamos e protegemos seus dados em todos os nossos aplicativos.</p>
                </a>

                <a href="politica.html#termos" class="legal-card">
                    <i class="fa-solid fa-file-contract"></i>
                    <h4>Termos de Uso (EULA)</h4>
                    <p>Regras de utilização, responsabilidades e licenças de software.</p>
                </a>

                <a href="politica.html#dados" class="legal-card">
                    <i class="fa-solid fa-database"></i>
                    <h4>Exclusão de Dados</h4>
                    <p>Solicite a remoção completa das suas informações dos nossos servidores.</p>
                </a>
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

    <a href="https://wa.me/5519981117451" class="whatsapp-float" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script> AOS.init(); </script>
</body>
</html>
    
