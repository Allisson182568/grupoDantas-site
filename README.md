<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    
    <meta name="google-adsense-account" content="ca-pub-3795771068897786">
    
    <meta name="description" content="Grupo Dantas - Especialistas em desenvolvimento de aplicativos iOS/Android, sistemas de gestão imobiliária e produção de conteúdo de tecnologia.">
    <meta name="keywords" content="desenvolvimento de apps, flutter, piracicaba, gestão imobiliária, tecnologia, nerdnews, ios developer">
    <meta name="author" content="Grupo Dantas">
    
    <title>Grupo Dantas | Desenvolvimento de Apps e Soluções Digitais</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Poppins:wght@500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3795771068897786"
     crossorigin="anonymous"></script>

    <style>
        /* --- CONFIGURAÇÕES VISUAIS --- */
        :root {
            --primary: #0f172a;
            --accent: #3b82f6;
            --accent-gradient: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            --secondary: #475569;
            --bg: #f8fafc;
            --blog-color: #e11d48;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        html { scroll-behavior: smooth; overflow-x: hidden; width: 100%; }
        body { 
            font-family: 'Inter', sans-serif; 
            background-color: var(--bg); 
            color: var(--primary); 
            line-height: 1.7; /* Aumentei para melhorar leitura */
            width: 100%;
            overflow-x: hidden;
        }
        h1, h2, h3 { font-family: 'Poppins', sans-serif; line-height: 1.3; }
        p { margin-bottom: 15px; font-size: 1rem; color: var(--secondary); }
        img { max-width: 100%; display: block; height: auto; }
        a { text-decoration: none; }

        /* --- HEADER --- */
        header { 
            background: rgba(255, 255, 255, 0.95); 
            backdrop-filter: blur(10px); 
            position: fixed; width: 100%; top: 0; z-index: 1000; 
            box-shadow: 0 4px 20px rgba(0,0,0,0.05); 
        }

        .container { width: 100%; max-width: 1100px; margin: 0 auto; padding: 0 20px; }

        .nav-wrapper { 
            display: flex; justify-content: space-between; align-items: center; height: 80px; 
        }

        .logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); white-space: nowrap; }
        .logo span { color: var(--accent); }
        
        .nav-buttons { display: flex; gap: 20px; align-items: center; }

        .btn-blog {
            color: var(--primary); font-weight: 600; font-size: 0.95rem; transition: color 0.3s;
            display: flex; align-items: center; gap: 6px;
        }
        .btn-blog:hover { color: var(--blog-color); }

        .btn-contact { 
            background: var(--accent-gradient); color: white; padding: 10px 24px; border-radius: 50px; 
            font-weight: 600; font-size: 0.95rem; white-space: nowrap; transition: transform 0.2s;
        }
        .btn-contact:hover { transform: translateY(-2px); box-shadow: 0 5px 15px rgba(59, 130, 246, 0.3); }

        /* --- HERO --- */
        .hero { padding: 140px 0 60px; text-align: center; }
        .hero h1 { font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 20px; font-weight: 800; }
        .hero p { max-width: 700px; margin: 0 auto 30px; font-size: 1.1rem; }

        /* --- SOBRE NÓS (TEXTO PARA GOOGLE) --- */
        .about-section {
            background: white; padding: 60px 0; border-radius: 20px; 
            margin-bottom: 80px; border: 1px solid #e2e8f0;
        }
        .about-content h2 { font-size: 2rem; margin-bottom: 20px; color: var(--primary); }

        /* --- PROJETOS --- */
        .project-card { display: flex; align-items: center; gap: 60px; margin-bottom: 100px; }
        .project-card.reverse { flex-direction: row-reverse; }
        .project-info { flex: 1; min-width: 0; }
        
        .tag { 
            background: #dbeafe; color: var(--accent); padding: 5px 12px; border-radius: 20px; 
            font-size: 0.8rem; font-weight: 700; text-transform: uppercase; margin-bottom: 15px; display: inline-block; 
        }
        .tag.news { background: #ffe4e6; color: var(--blog-color); }

        /* Descrições mais detalhadas para o Google ler */
        .project-desc { font-size: 1rem; line-height: 1.6; margin-bottom: 20px; }

        /* --- MOLDURAS (CSS Mantido e Otimizado) --- */
        .mockup-container { flex: 1; display: flex; justify-content: center; perspective: 1000px; padding: 10px; }

        .phone-frame { 
            width: 280px; height: auto; aspect-ratio: 9/19; 
            background: #1e293b; border-radius: 40px; padding: 10px; 
            box-shadow: 0 30px 60px -15px rgba(0,0,0,0.2); 
            transform: rotateY(-10deg) rotateX(5deg); transition: 0.5s; 
            position: relative; max-width: 100%; 
        }

        .macbook-frame {
            width: 100%; max-width: 550px; aspect-ratio: 16/10;
            background: #c7c7c7; border-radius: 16px; padding: 10px 10px 16px 10px; 
            box-shadow: 0 30px 60px -15px rgba(0,0,0,0.2);
            transform: rotateY(-10deg) rotateX(5deg); transition: 0.5s; 
            position: relative; display: flex;
        }
        
        .macbook-bezel {
            background: transparent; width: 100%; height: 100%;
            border-radius: 8px; padding: 0px; display: flex; overflow: hidden;
        }

        .phone-frame:hover, .macbook-frame:hover { transform: rotateY(0) rotateX(0) translateY(-10px); }
        .reverse .phone-frame, .reverse .macbook-frame { transform: rotateY(10deg) rotateX(5deg); }
        
        .screen { 
            width: 100%; height: 100%; background: #ffffff; 
            border-radius: 30px; overflow: hidden; position: relative;
        }
        .macbook-bezel .screen { border-radius: 6px; }
        .screen img { width: 100%; height: 100%; object-fit: cover; object-position: top center; }

        .features { padding-left: 0; margin-bottom: 20px; }
        .features li { margin-bottom: 8px; list-style: none; font-weight: 500; display: flex; align-items: center; }
        .features i { color: var(--accent); margin-right: 10px; font-size: 0.9rem; }

        /* --- FAQ SECTION (ESSENCIAL PARA APROVAÇÃO) --- */
        .faq-section { margin-bottom: 80px; }
        .faq-grid { display: grid; gap: 20px; margin-top: 30px; }
        .faq-item { background: white; padding: 25px; border-radius: 12px; border: 1px solid #e2e8f0; }
        .faq-item h4 { margin-bottom: 10px; color: var(--primary); font-size: 1.1rem; }
        .faq-item p { margin-bottom: 0; font-size: 0.95rem; }

        /* --- LEGAL & FOOTER --- */
        .legal-section { background: white; padding: 60px 0; border-top: 1px solid #e2e8f0; }
        .legal-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 30px; }
        .legal-card { 
            background: var(--bg); padding: 25px; border-radius: 12px; text-align: center; transition: 0.3s; 
            border: 1px solid #e2e8f0; display: block; color: var(--primary); 
        }
        .legal-card:hover { border-color: var(--accent); }
        
        footer { background: var(--primary); color: #94a3b8; padding: 60px 0 30px; text-align: center; }
        
        .whatsapp-float { 
            position: fixed; bottom: 30px; right: 30px; width: 60px; height: 60px; 
            background: #25d366; color: white; border-radius: 50%; 
            display: flex; align-items: center; justify-content: center; font-size: 30px; 
            box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4); z-index: 999; transition: transform 0.2s; 
        }
        .whatsapp-float:hover { transform: scale(1.1); }

        /* --- RESPONSIVIDADE --- */
        @media (max-width: 900px) {
            .nav-wrapper { height: 70px; }
            .hero { padding: 120px 0 40px; }
            .project-card, .project-card.reverse { flex-direction: column; text-align: center; gap: 40px; margin-bottom: 80px; }
            .features { display: inline-block; text-align: left; }
            .phone-frame, .reverse .phone-frame, .macbook-frame, .reverse .macbook-frame { transform: none !important; margin: 0 auto; }
        }

        @media (max-width: 480px) {
            .container { padding: 0 20px; }
            .nav-buttons { gap: 15px; }
            .btn-blog span { display: none; } 
            .btn-blog i { font-size: 1.4rem; color: var(--blog-color); }
            .btn-contact { padding: 8px 18px; font-size: 0.85rem; }
            .hero h1 { font-size: 2.2rem; } 
            
            .mockup-container { width: 100%; padding: 0; }
            .phone-frame { width: 100%; max-width: 260px; border-radius: 30px; }
            .macbook-frame { width: 100%; max-width: 340px; border-radius: 12px; }
            
            .legal-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-wrapper">
            <div class="logo">Grupo<span>Dantas</span></div>
            <div class="nav-buttons">
                <a href="https://nerdnews.grupodantass.com.br" target="_blank" class="btn-blog">
                    <i class="fa-solid fa-bolt"></i> <span>NerdNews</span>
                </a>
                <a href="https://wa.me/5519981117451" class="btn-contact">Orçamento</a>
            </div>
        </div>
    </header>

    <section class="hero">
        <div class="container" data-aos="fade-up">
            <h1>Transformamos ideias em<br><span style="color: var(--accent)">Aplicativos de Sucesso</span></h1>
            <p>Somos um estúdio de desenvolvimento focado em criar soluções digitais que funcionam. Desde apps imobiliários até ferramentas de produtividade para criadores de conteúdo.</p>
        </div>
    </section>

    <section class="container">
        <div class="about-section" data-aos="fade-up">
            <div class="container" style="max-width: 800px; text-align: center;">
                <h2>Tecnologia com Propósito</h2>
                <p>O <strong>Grupo Dantas</strong> nasceu da necessidade de simplificar processos complexos. Nossa missão é desenvolver softwares que não apenas resolvam problemas técnicos, mas que entreguem uma experiência de usuário fluida e intuitiva.</p>
                <p>Especialistas no ecossistema Apple (iOS) e Google (Android), utilizamos tecnologias modernas como Flutter e Firebase para garantir performance, segurança e escalabilidade em todos os nossos projetos.</p>
            </div>
        </div>
    </section>

    <section class="container" style="padding-bottom: 50px;">
        
        <div class="project-card" data-aos="fade-right">
            <div class="project-info">
                <span class="tag news">Portal de Conteúdo</span>
                <h3>NerdNews Tech</h3>
                <p class="project-desc">
                    O <strong>NerdNews</strong> é o braço de mídia e educação do Grupo Dantas. Um portal dedicado a cobrir as últimas inovações em tecnologia, inteligência artificial e desenvolvimento mobile.
                    Nossa redação produz análises profundas de gadgets, tutoriais de programação e resumos semanais do mercado tech.
                </p>
                <ul class="features">
                    <li><i class="fa-solid fa-bolt" style="color: var(--blog-color)"></i> Cobertura Apple & Android</li>
                    <li><i class="fa-solid fa-bolt" style="color: var(--blog-color)"></i> Tutoriais de Desenvolvimento</li>
                    <li><i class="fa-solid fa-bolt" style="color: var(--blog-color)"></i> Análises de Hardware</li>
                </ul>
                <div style="margin-top: 20px;">
                    <a href="https://nerdnews.grupodantass.com.br" target="_blank" style="color: var(--blog-color); font-weight: 700; border-bottom: 2px solid var(--blog-color);">Ler Matérias no Portal &rarr;</a>
                </div>
            </div>
            <div class="mockup-container">
                <div class="macbook-frame">
                    <div class="macbook-bezel">
                        <div class="screen">
                            <img src="blog.png" alt="Portal NerdNews Tech">
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card reverse" data-aos="fade-left">
            <div class="project-info">
                <span class="tag">SaaS Imobiliário</span>
                <h3>App Minha Kitnet</h3>
                <p class="project-desc">
                    Uma solução completa para proprietários de imóveis. O <strong>Minha Kitnet</strong> elimina as planilhas complexas, oferecendo um sistema automatizado para gestão de aluguéis, contratos e inquilinos.
                    Com foco na simplicidade, o app permite o envio de cobranças, monitoramento de vencimentos e geração de relatórios financeiros em tempo real.
                </p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Gestão de Contratos Digitais</li>
                    <li><i class="fa-solid fa-check"></i> Controle de Inadimplência</li>
                    <li><i class="fa-solid fa-check"></i> Backup Automático em Nuvem</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7993.png" alt="Interface App Minha Kitnet">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card" data-aos="fade-right">
            <div class="project-info">
                <span class="tag">Ferramenta de Design</span>
                <h3>Rotação Criativa</h3>
                <p class="project-desc">
                    Desenvolvido para designers e social media managers, o <strong>Rotação Criativa</strong> é uma suíte de edição mobile. Ele simplifica a criação de carrosséis infinitos e mockups profissionais diretamente pelo celular.
                    A ferramenta utiliza processamento de imagem avançado para garantir alta qualidade na exportação para redes sociais.
                </p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Editor de Panoramas</li>
                    <li><i class="fa-solid fa-check"></i> Templates de Mockups 3D</li>
                    <li><i class="fa-solid fa-check"></i> Exportação HD sem perdas</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7996.png" alt="App Rotação Criativa">
                    </div>
                </div>
            </div>
        </div>

        <div class="project-card reverse" data-aos="fade-left">
            <div class="project-info">
                <span class="tag">Utilitário para Devs</span>
                <h3>Smart Resizer</h3>
                <p class="project-desc">
                    Publicar aplicativos na App Store e Google Play exige screenshots em resoluções muito específicas. O <strong>Smart Resizer</strong> automatiza esse processo maçante.
                    Basta carregar uma imagem e o algoritmo redimensiona, corta e exporta todos os formatos obrigatórios (6.5", 5.5", 12.9") em segundos, poupando horas de trabalho dos desenvolvedores.
                </p>
                <ul class="features">
                    <li><i class="fa-solid fa-check"></i> Padrão Apple & Google Play</li>
                    <li><i class="fa-solid fa-check"></i> Processamento em Lote</li>
                    <li><i class="fa-solid fa-check"></i> Interface Drag & Drop</li>
                </ul>
            </div>
            <div class="mockup-container">
                <div class="phone-frame">
                    <div class="screen">
                        <img src="IMG_7997.png" alt="App Smart Resizer">
                    </div>
                </div>
            </div>
        </div>

    </section>

    <section class="container faq-section">
        <h2 style="text-align: center; margin-bottom: 30px;">Perguntas Frequentes</h2>
        <div class="faq-grid">
            <div class="faq-item">
                <h4>O Grupo Dantas desenvolve aplicativos sob demanda?</h4>
                <p>Sim. Além de nossos produtos próprios, atuamos como consultoria técnica para empresas que desejam tirar suas ideias do papel, oferecendo desde o design UI/UX até o desenvolvimento e publicação nas lojas.</p>
            </div>
            <div class="faq-item">
                <h4>Como funciona a política de privacidade dos apps?</h4>
                <p>Levamos a segurança a sério. Nenhum de nossos aplicativos coleta dados sensíveis sem consentimento explícito. Utilizamos criptografia de ponta a ponta e seguimos rigorosamente a LGPD.</p>
            </div>
            <div class="faq-item">
                <h4>O portal NerdNews é atualizado com que frequência?</h4>
                <p>Nossa equipe editorial publica matérias diariamente, cobrindo os principais eventos de tecnologia do mundo, lançamentos de hardware e atualizações de software.</p>
            </div>
        </div>
    </section>

    <section class="legal-section">
        <div class="container">
            <div style="text-align: center; max-width: 600px; margin: 0 auto;">
                <h2 style="font-size: 1.5rem; margin-bottom: 10px;">Transparência</h2>
                <p style="color: var(--secondary);">Documentação legal e termos de uso.</p>
            </div>

            <div class="legal-grid">
                <a href="https://allisson182568.github.io/grupoDantas-site/politica.html" class="legal-card">
                    <i class="fa-solid fa-shield-halved"></i>
                    <h4>Política de Privacidade</h4>
                </a>
                <a href="https://allisson182568.github.io/grupoDantas-site/politica.html#termos" class="legal-card">
                    <i class="fa-solid fa-file-contract"></i>
                    <h4>Termos de Uso</h4>
                </a>
                <a href="https://allisson182568.github.io/grupoDantas-site/politica.html#dados" class="legal-card">
                    <i class="fa-solid fa-database"></i>
                    <h4>Exclusão de Dados</h4>
                </a>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="logo" style="color: white; margin-bottom: 20px;">Grupo<span>Dantas</span></div>
            <p>Inovação e tecnologia para o seu dia a dia.</p>
            <br>
            <a href="ads.txt" style="color: #94a3b8; font-size: 0.8rem; border: 1px solid #334155; padding: 5px 10px; border-radius: 5px; margin-right: 10px;">AdSense Check</a>
            <a href="app-ads.txt" style="color: #94a3b8; font-size: 0.8rem; border: 1px solid #334155; padding: 5px 10px; border-radius: 5px;">AdMob Check</a>
            <p style="margin-top: 30px; font-size: 0.8rem; color: #475569;">&copy; 2026 Grupo Dantas. Piracicaba/SP.</p>
        </div>
    </footer>

    <a href="https://wa.me/5519981117451" class="whatsapp-float" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script> AOS.init({ duration: 800, once: true }); </script>
</body>
</html>
