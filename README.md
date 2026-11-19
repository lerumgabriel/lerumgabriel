    body {
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
        color: var(--gh-text);
        margin: 0;
        padding: 0;
        line-height: 1.6;
        
        /* DARK MODE BACKGROUND + IMAGE */
        background-image: linear-gradient(rgba(13, 17, 23, 0.85), rgba(13, 17, 23, 0.90)), 
                          url('nature-castle.gif'); 
        background-size: cover;
        background-position: center;
        background-attachment: fixed;
        background-color: var(--gh-bg);
    }
    
    /* --- ANIMATIONS --- */
    @keyframes fadeInSlideUp {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    @keyframes pulseGlow {
        0% { box-shadow: 0 0 0 0 rgba(88, 166, 255, 0.4); }
        70% { box-shadow: 0 0 0 10px rgba(88, 166, 255, 0); }
        100% { box-shadow: 0 0 0 0 rgba(88, 166, 255, 0); }
    }

    /* --- NAVBAR & LAYOUT --- */
    .navbar {
        background-color: #010409;
        padding: 16px 24px;
        color: white;
        font-weight: 600;
        display: flex;
        align-items: center;
        border-bottom: 1px solid var(--gh-border);
    }
    .container {
        max-width: 1200px;
        margin: 32px auto;
        padding: 0 24px;
        display: flex;
        gap: 32px;
        animation: fadeInSlideUp 0.8s ease-out forwards;
    }
    
    /* --- SIDEBAR --- */
    .sidebar {
        width: 296px;
        flex-shrink: 0;
    }
    .profile-pic {
        width: 296px;
        height: 296px;
        border-radius: 50%;
        border: 1px solid var(--gh-border);
        background-color: var(--gh-header-bg);
        margin-bottom: 16px;
        object-fit: cover;
        animation: pulseGlow 3s infinite;
        transition: transform 0.3s ease;
    }
    .profile-pic:hover {
        transform: scale(1.02);
    }
    .names h1 { font-size: 26px; margin: 0; line-height: 1.25; color: white; }
    .names h2 { font-size: 20px; color: var(--gh-muted); font-weight: 300; margin: 0 0 16px 0; }
    .bio { font-size: 15px; margin-bottom: 16px; color: var(--gh-text); }
    .details-list { list-style: none; padding: 0; margin: 0; font-size: 14px; }
    .details-list li { padding: 4px 0; display: flex; align-items: center; gap: 8px; }

    /* --- MAIN CONTENT & README --- */
    .main-content { flex-grow: 1; }
    
    .readme { 
        border: 1px solid var(--gh-border); 
        border-radius: 8px; 
        margin-bottom: 32px; 
        background-color: rgba(13, 17, 23, 0.6);
        backdrop-filter: blur(10px);
    }
    .readme-header { 
        padding: 12px 24px; 
        border-bottom: 1px solid var(--gh-border); 
        font-weight: 600; 
        background-color: rgba(22, 27, 34, 0.8); 
        font-size: 14px; 
        border-radius: 8px 8px 0 0;
    }
    .readme-content { padding: 32px 40px; }
    .readme-content h2 { margin-top: 0; padding-bottom: 8px; border-bottom: 1px solid var(--gh-border); color: white; }
    
    /* --- LANGUAGE BADGES --- */
    .lang-badge {
        display: inline-block;
        padding: 6px 16px;
        border-radius: 20px;
        font-size: 13px;
        font-weight: 600;
        margin: 0 4px 8px 4px;
        border: 1px solid var(--gh-border);
        text-transform: uppercase;
        letter-spacing: 0.5px;
    }
    .lang-java { background-color: rgba(176, 114, 25, 0.1); color: #e8a03c; border-color: #b07219; }
    .lang-python { background-color: rgba(53, 114, 165, 0.1); color: #58a6ff; border-color: #3572A5; }
    .lang-html { background-color: rgba(227, 76, 38, 0.1); color: #ff7b5c; border-color: #e34c26; }

    /* --- NEW: INTERACTIVE PROJECT GRID --- */
    .repo-header { 
        font-size: 22px; 
        color: white; 
        margin-bottom: 8px; 
        font-weight: 600; 
    }
    .repo-header span { color: var(--gh-muted); font-weight: 400; }
    .section-desc {
        color: var(--gh-muted);
        font-size: 15px;
        margin-bottom: 24px;
    }

    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 16px;
        margin-bottom: 40px;
    }

    .project-card {
        background-color: rgba(22, 27, 34, 0.7);
        border: 1px solid var(--gh-border);
        border-radius: 8px;
        padding: 24px;
        text-decoration: none;
        color: var(--gh-text);
        transition: all 0.3s ease;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        backdrop-filter: blur(5px);
    }

    /* Cyberpunk Hover Effect */
    .project-card:hover {
        transform: translateY(-5px);
        border-color: var(--gh-link);
        box-shadow: 0 0 15px rgba(88, 166, 255, 0.15), inset 0 0 20px rgba(88, 166, 255, 0.05);
    }

    .project-card h3 {
        margin: 0 0 12px 0;
        color: var(--gh-link);
        font-size: 18px;
        display: flex;
        align-items: center;
        gap: 8px;
    }

    .project-card p {
        margin: 0;
        color: var(--gh-muted);
        font-size: 14px;
        line-height: 1.5;
        flex-grow: 1;
    }

    .project-card .footer {
        margin-top: 20px;
        font-size: 12px;
        color: var(--gh-muted);
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-top: 1px solid var(--gh-border);
        padding-top: 12px;
    }
    
    .footer .arrow {
        color: var(--gh-link);
        font-weight: 600;
        opacity: 0;
        transition: opacity 0.3s ease, transform 0.3s ease;
        transform: translateX(-10px);
    }

    .project-card:hover .footer .arrow {
        opacity: 1;
        transform: translateX(0);
    }
</style>## Hi there 👋

<!--
**lerumgabriel/lerumgabriel** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
