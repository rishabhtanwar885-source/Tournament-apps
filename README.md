<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>INDIA BATTLE</title>
    <meta name="description" content="Esports tournament and gaming contest platform with Ongoing, Upcoming, and Completed match tracking." />
    <meta property="og:title" content="INDIA BATTLE" />
    <meta property="og:description" content="Esports tournament and gaming contest platform with Ongoing, Upcoming, and Completed match tracking." />
    <meta property="og:type" content="website" />

    <!-- Icons and Modern Font -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Bootstrap & ZapUPI SDK -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://zapupi.com/single-html-web-kit.js"></script>

    <style>
        /* =========================================
           1. PREMIUM 7 THEMES (CSS VARIABLES)
        ========================================= */
        body.theme-neon { --bg-base: #000000; --bg-surface: rgba(5, 15, 5, 0.7); --bg-card: #080808; --text-main: #39ff14; --text-muted: #85d885; --accent-cyan: #00ffff; --accent-purple: #ff00ff; --accent-gold: #ffff00; --gradient-primary: linear-gradient(135deg, #39ff14, #00ffff); --gradient-gold: linear-gradient(135deg, #ffff00, #ffaa00); --border-glass: rgba(57, 255, 20, 0.25); --glow-shadow: 0 0 15px rgba(57, 255, 20, 0.35); --ph-bg-1: #050505; --ph-bg-2: #151515; --bg-img: radial-gradient(circle at top right, rgba(57, 255, 20, 0.1), transparent 40%), radial-gradient(circle at bottom left, rgba(0, 255, 255, 0.1), transparent 40%); }
        body.theme-cyber { --bg-base: #020617; --bg-surface: rgba(15, 23, 42, 0.75); --bg-card: #0b1120; --text-main: #e2e8f0; --text-muted: #94a3b8; --accent-cyan: #0ea5e9; --accent-purple: #6366f1; --accent-gold: #f59e0b; --gradient-primary: linear-gradient(135deg, #0ea5e9, #8b5cf6); --gradient-gold: linear-gradient(135deg, #f59e0b, #fbbf24); --border-glass: rgba(14, 165, 233, 0.25); --glow-shadow: 0 0 15px rgba(14, 165, 233, 0.35); --ph-bg-1: #0f172a; --ph-bg-2: #1e293b; --bg-img: radial-gradient(circle at top right, rgba(14, 165, 233, 0.1), transparent 40%), radial-gradient(circle at bottom left, rgba(99, 102, 241, 0.1), transparent 40%); }
        body.theme-purple { --bg-base: #17002e; --bg-surface: rgba(43, 0, 87, 0.65); --bg-card: #200042; --text-main: #f3e8ff; --text-muted: #d8b4fe; --accent-cyan: #a855f7; --accent-purple: #ec4899; --accent-gold: #eab308; --gradient-primary: linear-gradient(135deg, #a855f7, #ec4899); --gradient-gold: linear-gradient(135deg, #eab308, #facc15); --border-glass: rgba(168, 85, 247, 0.25); --glow-shadow: 0 0 15px rgba(168, 85, 247, 0.35); --ph-bg-1: #2b0057; --ph-bg-2: #4c1d95; --bg-img: radial-gradient(circle at top right, rgba(168, 85, 247, 0.15), transparent 40%), radial-gradient(circle at bottom left, rgba(236, 72, 153, 0.1), transparent 40%); }
        body.theme-red { --bg-base: #1a0505; --bg-surface: rgba(69, 10, 10, 0.7); --bg-card: #2e0808; --text-main: #fecaca; --text-muted: #fca5a5; --accent-cyan: #ef4444; --accent-purple: #dc2626; --accent-gold: #f59e0b; --gradient-primary: linear-gradient(135deg, #ef4444, #f97316); --gradient-gold: linear-gradient(135deg, #f59e0b, #fbbf24); --border-glass: rgba(239, 68, 68, 0.25); --glow-shadow: 0 0 15px rgba(239, 68, 68, 0.35); --ph-bg-1: #450a0a; --ph-bg-2: #7f1d1d; --bg-img: radial-gradient(circle at top right, rgba(239, 68, 68, 0.1), transparent 40%), radial-gradient(circle at bottom left, rgba(249, 115, 22, 0.1), transparent 40%); }
        body.theme-gold { --bg-base: #1c1917; --bg-surface: rgba(41, 37, 36, 0.8); --bg-card: #292524; --text-main: #fef08a; --text-muted: #fde047; --accent-cyan: #eab308; --accent-purple: #ca8a04; --accent-gold: #f59e0b; --gradient-primary: linear-gradient(135deg, #eab308, #d97706); --gradient-gold: linear-gradient(135deg, #eab308, #facc15); --border-glass: rgba(234, 179, 8, 0.25); --glow-shadow: 0 0 15px rgba(234, 179, 8, 0.35); --ph-bg-1: #292524; --ph-bg-2: #44403c; --bg-img: radial-gradient(circle at top right, rgba(234, 179, 8, 0.1), transparent 40%), radial-gradient(circle at bottom left, rgba(217, 119, 6, 0.1), transparent 40%); }
        body.theme-dark { --bg-base: #09090b; --bg-surface: rgba(24, 24, 27, 0.75); --bg-card: #18181b; --text-main: #fafafa; --text-muted: #a1a1aa; --accent-cyan: #06b6d4; --accent-purple: #8b5cf6; --accent-gold: #facc15; --gradient-primary: linear-gradient(135deg, var(--accent-cyan), var(--accent-purple)); --gradient-gold: linear-gradient(135deg, #facc15, #f59e0b); --border-glass: rgba(255, 255, 255, 0.08); --glow-shadow: 0 4px 20px rgba(0,0,0,0.4); --ph-bg-1: #18181b; --ph-bg-2: #27272a; --bg-img: radial-gradient(circle at top right, rgba(139, 92, 246, 0.1), transparent 40%), radial-gradient(circle at bottom left, rgba(6, 182, 212, 0.08), transparent 40%); }
        body.theme-light { --bg-base: #f4f4f5; --bg-surface: rgba(255, 255, 255, 0.85); --bg-card: #ffffff; --text-main: #18181b; --text-muted: #71717a; --accent-cyan: #0891b2; --accent-purple: #7c3aed; --accent-gold: #d97706; --gradient-primary: linear-gradient(135deg, var(--accent-cyan), var(--accent-purple)); --gradient-gold: linear-gradient(135deg, #facc15, #d97706); --border-glass: rgba(0, 0, 0, 0.1); --glow-shadow: 0 4px 15px rgba(0,0,0,0.08); --ph-bg-1: #e4e4e7; --ph-bg-2: #f4f4f5; --bg-img: radial-gradient(circle at top right, rgba(124, 58, 237, 0.06), transparent 40%), radial-gradient(circle at bottom left, rgba(8, 145, 178, 0.06), transparent 40%); }
        
        /* Light Mode Specific Resets */
        body.theme-light .btn-close-white { filter: none !important; opacity: 0.6; }
        
        :root { --radius-md: 12px; --radius-lg: 16px; --radius-xl: 20px; }

        /* =========================================
           2. GLOBAL RESETS & TYPOGRAPHY
        ========================================= */
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        html { font-size: 15px; scroll-behavior: smooth; overflow-x: hidden; }
        body { font-family: 'Plus Jakarta Sans', sans-serif; background-color: var(--bg-base); color: var(--text-main); padding-top: 80px; padding-bottom: 100px; min-height: 100vh; background-image: var(--bg-img); background-attachment: fixed; overflow-x: hidden; transition: background-color 0.4s ease, color 0.4s ease; }
        .text-main { color: var(--text-main) !important; }
        .text-gradient { background: var(--gradient-primary); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: 800; }
        .glow-text { text-shadow: var(--glow-shadow); }

        /* Heading Dynamic Color Rule */
        .section-title, h1, h2, h3, h4, h5, h6 { color: var(--text-heading, var(--text-main)) !important; }

        .glass-card, .btn-custom, .bottom-nav, .section { transform: translateZ(0); will-change: transform, opacity; }

        /* =========================================
           3. UI COMPONENTS & ANIMATIONS
        ========================================= */
        .main-content { padding: 0 16px; max-width: 500px; margin: 0 auto; width: 100%; } 
        .section { display: none; opacity: 0; } 
        .section.active { display: block; animation: fadeSlideUp 0.35s cubic-bezier(0.2, 0.8, 0.2, 1) forwards; } 
        @keyframes fadeSlideUp { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }

        .section-title { font-size: 1.15rem; font-weight: 800; margin-bottom: 16px; display: flex; align-items: center; gap: 8px; text-transform: uppercase; letter-spacing: 0.5px;} 
        
        .glass-card { background: var(--bg-surface); backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); border-radius: var(--radius-lg); padding: 16px; margin-bottom: 16px; border: 1px solid var(--border-glass); box-shadow: var(--glow-shadow); transition: all 0.3s ease; } 
        
        .btn-custom { border-radius: 12px; font-size: 0.95rem; font-weight: 700; padding: 12px 20px; border: none; display: inline-flex; align-items: center; justify-content: center; gap: 8px; transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1); color: white; width: 100%; position: relative; overflow: hidden; } 
        .btn-primary-gradient { background: var(--btn-custom-bg, var(--gradient-primary)); box-shadow: var(--glow-shadow); color: #fff !important; }
        .btn-primary-gradient:active { transform: scale(0.96); box-shadow: none; }
        .btn-outline-custom { background: rgba(128,128,128,0.05); border: 1px solid var(--border-glass); color: var(--text-main); }
        .btn-outline-custom:active { background: rgba(128,128,128,0.15); transform: scale(0.96); }
        .btn-hover-glow:hover { box-shadow: var(--glow-shadow); }
        
        .form-control { background-color: rgba(128,128,128,0.1); border: 1px solid var(--border-glass); color: var(--text-main); border-radius: 12px; padding: 12px 16px; font-size: 0.95rem; transition: 0.3s; } 
        .form-control:focus { background-color: rgba(128,128,128,0.15); border-color: var(--accent-cyan); color: var(--text-main); box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.2); outline: none;} 
        .form-control::placeholder { color: var(--text-muted); } 
        .form-label { color: var(--text-muted); font-size: 0.8rem; font-weight: 700; margin-bottom: 6px; text-transform: uppercase; letter-spacing: 0.5px; } 

        .games-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
        .game-card-new { aspect-ratio: 1 / 1.25; border-radius: var(--radius-md); background-size: cover; background-position: center; position: relative; overflow: hidden; border: 1px solid var(--border-glass); cursor: pointer; transition: transform 0.2s; box-shadow: var(--glow-shadow);}
        .game-card-new:active { transform: scale(0.95); }
        .game-card-new-overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(0,0,0,0.95) 0%, transparent 60%); display: flex; align-items: flex-end; padding: 10px 8px; pointer-events: none;}
        .game-card-new-overlay span { color: white; font-weight: 800; font-size: 0.8rem; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; width: 100%; text-align: center; }

        /* MY CONTESTS 3-CARD GRID (ONGOING / UPCOMING / RESULTS) */
        .my-contests-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-bottom: 22px; }
        .contest-status-card {
            background: var(--bg-card);
            border: 1px solid var(--border-glass);
            border-radius: var(--radius-lg);
            padding: 18px 8px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 10px;
            cursor: pointer;
            transition: transform 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease;
            box-shadow: var(--glow-shadow);
            position: relative;
            text-align: center;
            user-select: none;
        }
        .contest-status-card:active { transform: scale(0.95); }
        .contest-status-card i { font-size: 1.55rem; line-height: 1; }
        .contest-status-card .contest-card-label { font-size: 0.85rem; font-weight: 700; color: var(--text-main); line-height: 1.2; }
        .contest-status-card.ongoing-card i { color: #ef4444; filter: drop-shadow(0 0 6px rgba(239, 68, 68, 0.45)); }
        .contest-status-card.upcoming-card i { color: #facc15; filter: drop-shadow(0 0 6px rgba(250, 204, 21, 0.45)); }
        .contest-status-card.completed-card i { color: #22c55e; filter: drop-shadow(0 0 6px rgba(34, 197, 94, 0.45)); }

        .modes-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; }
        .mode-card { border-radius: var(--radius-md); background-size: cover; background-position: center; position: relative; overflow: hidden; border: 1px solid var(--border-glass); cursor: pointer; transition: transform 0.2s; box-shadow: var(--glow-shadow); aspect-ratio: 16/9; }
        .mode-card:active { transform: scale(0.95); }
        .mode-card-overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, transparent 70%); display: flex; align-items: flex-end; padding: 12px 10px; pointer-events: none; }
        .mode-card-overlay span { color: white; font-weight: 800; font-size: 0.95rem; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; width: 100%; text-shadow: 0 2px 4px rgba(0,0,0,0.8); }

        .custom-toast { position: fixed; bottom: 90px; left: 50%; transform: translateX(-50%) translateY(20px); background: var(--bg-card); border: 1px solid var(--accent-cyan); padding: 12px 20px; border-radius: 30px; font-weight: 700; font-size: 0.9rem; color: var(--text-main); box-shadow: var(--glow-shadow); z-index: 10000; opacity: 0; visibility: hidden; transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55); white-space: nowrap;}
        .custom-toast.show { opacity: 1; visibility: visible; transform: translateX(-50%) translateY(0); }
        .toast-error { border-color: #ef4444; color: #ef4444; box-shadow: 0 0 15px rgba(239, 68, 68, 0.4);}
        .toast-success { border-color: #10b981; color: #10b981; box-shadow: 0 0 15px rgba(16, 185, 129, 0.4);}

        /* =========================================
           4. HEADER & BOTTOM NAV
        ========================================= */
        .app-header { position: fixed; top: 0; left: 50%; transform: translateX(-50%); width: 100%; max-width: 500px; height: 65px; background: var(--bg-surface); backdrop-filter: blur(15px); -webkit-backdrop-filter: blur(15px); display: flex; align-items: center; justify-content: space-between; padding: 0 16px; z-index: 1000; border-bottom: 1px solid var(--border-glass); box-shadow: 0 2px 20px rgba(0,0,0,0.2); } 
        .header-logo { width: 36px; height: 36px; border-radius: 10px; border: 1px solid var(--accent-cyan); object-fit: cover; box-shadow: 0 0 8px var(--accent-cyan); } 
        .header-title { font-size: 1.1rem; font-weight: 800; text-transform: uppercase; white-space: nowrap; overflow: hidden; display: flex; flex-direction: column; line-height: 1.2;} 
        .header-title small { font-size: 0.7rem; color: var(--accent-cyan); font-weight: 700; text-transform: none; }
        
        .wallet-chip { background: rgba(128,128,128,0.1); backdrop-filter: blur(10px); color: var(--text-main); padding: 6px 14px; border-radius: 12px; display: flex; align-items: center; font-size: 0.95rem; font-weight: 800; border: 1px solid var(--border-glass); cursor: pointer; height: 40px; transition: all 0.2s; box-shadow: var(--glow-shadow); } 
        .wallet-chip:active { transform: scale(0.95); }
        .wallet-chip i { color: var(--accent-cyan); margin-right: 6px; font-size: 1.1rem; filter: drop-shadow(0 0 3px var(--accent-cyan));}

        .bottom-nav { position: fixed; bottom: 16px; left: 50%; transform: translateX(-50%); width: calc(100% - 32px); max-width: 468px; height: 65px; background: var(--bg-surface); backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px); display: flex; justify-content: space-around; align-items: center; border-radius: var(--radius-xl); border: 1px solid var(--border-glass); box-shadow: var(--glow-shadow); z-index: 1000; padding: 0 8px; } 
        .nav-item { display: flex; flex-direction: column; align-items: center; justify-content: center; color: var(--text-muted); text-decoration: none; padding: 4px; flex: 1; background: none; border: none; cursor: pointer; font-size: 0.7rem; font-weight: 600; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); } 
        .nav-item i { font-size: 1.3rem; margin-bottom: 2px; transition: 0.3s; } 
        .nav-item.active { color: var(--text-main); transform: translateY(-4px); } 
        .nav-item.active i { color: var(--accent-cyan); filter: drop-shadow(0 0 8px var(--accent-cyan)); }
        
        @keyframes neonPulseCenter { 0% { box-shadow: 0 0 10px var(--accent-cyan); } 50% { box-shadow: 0 0 25px var(--accent-cyan), 0 0 10px var(--accent-purple); } 100% { box-shadow: 0 0 10px var(--accent-cyan); } }
        .nav-item.nav-item-center { transform: translateY(-22px); background: var(--gradient-primary); color: white; border-radius: 50%; width: 55px; height: 55px; border: 4px solid var(--bg-base); animation: neonPulseCenter 2.5s infinite alternate; z-index: 1001; flex: none; }
        .nav-item.nav-item-center i { font-size: 1.6rem; margin: 0; color: white; }
        .nav-item.nav-item-center span { display: none; }
        .nav-item.nav-item-center:active { transform: translateY(-20px) scale(0.95); animation: none; box-shadow: none; }

        /* =========================================
           5. OTHER STYLES
        ========================================= */
        .glowing-card { border: 1px solid var(--accent-cyan); box-shadow: inset 0 0 20px rgba(0,255,255,0.05), 0 0 15px rgba(0,255,255,0.2); position: relative; overflow: hidden; }
        .particles-bg { position: absolute; inset: 0; pointer-events: none; opacity: 0.4; background-image: radial-gradient(var(--accent-cyan) 1px, transparent 1px); background-size: 20px 20px; animation: floatParticles 15s linear infinite; }
        @keyframes floatParticles { 0% { background-position: 0 0; } 100% { background-position: 100px 100px; } }

        .theme-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-bottom: 20px; }
        .theme-card-select { cursor: pointer; border-radius: var(--radius-md); padding: 14px 10px; border: 2px solid var(--border-glass); background: rgba(128,128,128,0.05); transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); text-align: center; color: var(--text-muted); position: relative; }
        .theme-card-select.active { border-color: var(--accent-cyan); background: rgba(128,128,128,0.15); color: var(--text-main); box-shadow: var(--glow-shadow); transform: translateY(-2px); }
        .theme-indicator { width: 32px; height: 32px; border-radius: 50%; margin: 0 auto 8px; display: flex; align-items: center; justify-content: center; border: 2px solid rgba(255,255,255,0.2); }

        .list-group-item { background: transparent; color: var(--text-main); border: none; border-bottom: 1px solid var(--border-glass); padding: 16px 12px; font-size: 0.95rem; font-weight: 600; transition: 0.2s; cursor: pointer; text-decoration: none; display: flex; justify-content: space-between; align-items: center;} 
        .list-group-item:active { background: rgba(128,128,128,0.1); } 
        .list-group-item:last-child { border-bottom: none; }
        .list-group-item i:first-child { color: var(--accent-purple); margin-right: 12px; font-size: 1.2rem; filter: drop-shadow(0 0 5px var(--accent-purple)); }
        
        /* Loading Shimmer Effects */
        .placeholder-glow .placeholder { background: linear-gradient(90deg, var(--ph-bg-1) 25%, var(--ph-bg-2) 50%, var(--ph-bg-1) 75%); background-size: 200% 100%; animation: shimmer 1.5s infinite linear; border-radius: var(--radius-md); opacity: 1; }
        @keyframes shimmer { 0% { background-position: -200% 0; } 100% { background-position: 200% 0; } }
        
        .tournament-tabs { display: flex; background: rgba(128,128,128,0.1); padding: 4px; border-radius: var(--radius-xl); margin-bottom: 20px; border: 1px solid var(--border-glass); } 
        .tab-item { color: var(--text-muted); background: none; border: none; padding: 10px; font-size: 0.85rem; font-weight: 700; border-radius: var(--radius-xl); flex: 1; text-align: center; transition: 0.3s; } 
        .tab-item.active { background: var(--bg-card); color: var(--text-main); border: 1px solid var(--border-glass); box-shadow: var(--glow-shadow);}

        .tournament-card { background: var(--bg-card); border-radius: var(--radius-lg); margin-bottom: 20px; border: 1px solid var(--border-glass); overflow: hidden; box-shadow: var(--glow-shadow); position: relative; }
        .tournament-banner-image { width: 100%; aspect-ratio: 21/9; object-fit: cover; }
        .tournament-card-content { padding: 16px; }
        
        .modal-content { background: var(--bg-card); border-radius: var(--radius-lg); border: 1px solid var(--border-glass); color: var(--text-main); box-shadow: var(--glow-shadow); }
        
        /* Premium Accordion for Rules & Policies */
        .premium-accordion .accordion-item { background: var(--bg-surface); border: 1px solid var(--border-glass); border-radius: var(--radius-md) !important; margin-bottom: 12px; backdrop-filter: blur(10px); -webkit-backdrop-filter: blur(10px); overflow: hidden; box-shadow: var(--glow-shadow); transition: all 0.3s ease; }
        .premium-accordion .accordion-button { background: transparent !important; color: var(--text-main) !important; font-weight: 700; box-shadow: none !important; padding: 16px 20px; gap: 12px; }
        .premium-accordion .accordion-button::after { filter: brightness(0) invert(1); opacity: 0.6; }
        .premium-accordion .accordion-button:not(.collapsed)::after { filter: brightness(0) invert(1) drop-shadow(0 0 5px var(--accent-cyan)); opacity: 1; }
        .premium-accordion .accordion-body { color: var(--text-muted); padding: 0 20px 20px 20px; line-height: 1.6; font-size: 0.9rem; background: transparent; }
        .premium-accordion .accordion-button:not(.collapsed) { color: var(--accent-cyan) !important; }

        /* Helpers & New Features styling */
        .last-border-none:last-child { border-bottom: none !important; }
        .prize-click-area { cursor: pointer; transition: background 0.2s ease, transform 0.1s; }
        .prize-click-area:active { background: rgba(128,128,128,0.2) !important; transform: scale(0.95); }

        /* =========================================
           6. PREMIUM ANNOUNCEMENT BAR
        ========================================= */
        .announcement-bar {
            background: rgba(168, 85, 247, 0.1);
            border: 1px solid rgba(168, 85, 247, 0.3);
            border-radius: 50px;
            box-shadow: 0 0 15px rgba(168, 85, 247, 0.2);
            padding: 8px 16px;
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
        }
        .announcement-icon {
            color: #a855f7;
            font-size: 1.2rem;
            margin-right: 12px;
            filter: drop-shadow(0 0 8px #a855f7);
            z-index: 2;
        }
        .announcement-marquee {
            flex: 1;
            overflow: hidden;
            white-space: nowrap;
            position: relative;
            mask-image: linear-gradient(to right, transparent, black 5%, black 95%, transparent);
            -webkit-mask-image: linear-gradient(to right, transparent, black 5%, black 95%, transparent);
        }
        .announcement-text {
            display: inline-block;
            padding-left: 100%;
            animation: marquee-scroll linear infinite;
            color: var(--text-main);
            font-weight: 600;
            font-size: 0.9rem;
            letter-spacing: 0.5px;
        }
        @keyframes marquee-scroll {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-100%, 0); }
        }
       
       /* =========================================
           7. FULL SCREEN NOTIFICATION OVERLAY
        ========================================= */
        .notification-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--bg-base);
            z-index: 99999;
            display: flex;
            flex-direction: column;
            opacity: 0;
            visibility: hidden;
            transform: translateX(100%);
            transition: all 0.3s cubic-bezier(0.2, 0.8, 0.2, 1);
        }
        
        .notification-overlay.show {
            opacity: 1;
            visibility: visible;
            transform: translateX(0);
        }
        
        .notification-header {
            height: 65px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 16px;
            background: var(--bg-surface);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border-bottom: 1px solid var(--border-glass);
            box-shadow: 0 2px 20px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 2;
        }
        
        .notification-header h3 {
            color: var(--text-main);
            margin: 0;
            font-size: 1.15rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            flex-grow: 1;
            text-align: center;
        }
        
        .notification-header button {
            background: none;
            border: none;
            color: var(--text-main);
            font-size: 1.8rem;
            padding: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s;
        }

        .notification-header button:active {
            transform: scale(0.9);
        }
        
        .notification-list {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            background-image: var(--bg-img);
            background-attachment: fixed;
            position: relative;
        }

        /* =========================================
           8. ESPORTS SLOT SYSTEM
        ========================================= */
        .esports-slot-grid { display: flex; flex-direction: column; gap: 10px; max-height: 280px; overflow-y: auto; padding-right: 5px; }
        .esports-team-row { display: flex; align-items: center; justify-content: space-between; padding: 10px 14px; background: rgba(128,128,128,0.05); border: 1px solid var(--border-glass); border-radius: 8px; transition: 0.2s; }
        .esports-team-name { font-weight: 800; font-size: 0.85rem; color: var(--text-muted); width: 60px; }
        .esports-slots { display: flex; gap: 8px; flex-wrap: wrap; flex: 1; justify-content: flex-end; }
        .slot-item { width: 38px; height: 38px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-weight: bold; font-size: 0.85rem; cursor: pointer; transition: all 0.2s; border: 1px solid; }
        .slot-available { border-color: #10b981; color: #10b981; background: rgba(16, 185, 129, 0.1); }
        .slot-selected { border-color: var(--accent-cyan); color: #fff; background: var(--accent-cyan); box-shadow: 0 0 12px var(--accent-cyan); transform: scale(1.05); }
        .slot-booked { border-color: #4b5563; color: #6b7280; background: rgba(75, 85, 99, 0.2); cursor: not-allowed; }
        .team-full { background: rgba(239, 68, 68, 0.05); border-color: rgba(239, 68, 68, 0.3); }
        .team-full .esports-team-name { color: #ef4444; }
        .solo-slot-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(45px, 1fr)); gap: 10px; max-height: 280px; overflow-y: auto; padding-right: 5px; }

    </style>

    <script>
        // Priority: User Override > App Theme Default > Fallback
        (function() {
            const userOverride = localStorage.getItem("user_override_theme");
            const savedTheme = userOverride || localStorage.getItem("app_theme") || "theme-neon";
            document.body.className = savedTheme;
        })();
    </script>
<script src="/_aistudio-iframe.js?v=29045eb3"></script></head>

<body class="theme-neon">
    <!-- Global Notifications & UI Helpers -->
    <div id="globalToast" class="custom-toast">Message</div>
    <div id="globalLoaderEl" style="position: fixed; inset: 0; background: var(--bg-base); z-index: 9999; display: flex; justify-content: center; align-items: center; flex-direction: column;">
        <div class="spinner-border glow-text" style="color: var(--accent-cyan); width: 3rem; height: 3rem;" role="status"></div>
        <div class="mt-3 fw-bold text-uppercase" style="color: var(--accent-cyan); letter-spacing: 2px; font-size: 0.9rem;" data-i18n="loading">Loading...</div>
    </div>

    <!-- Header -->
    <header class="app-header">
        <div class="header-left d-flex align-items-center flex-fill overflow-hidden gap-2">
            <button class="btn-custom-link" id="headerBackBtnEl" style="font-size: 1.8rem; display: none; color: var(--text-main); padding-right:10px; background:transparent; border:none;"><i class="bi bi-arrow-left-short glow-text"></i></button>
            <img src="https://via.placeholder.com/100/18181b/06b6d4?text=LOGO" alt="Logo" class="header-logo app-logo-img" id="appLogoEl">
            <div class="header-title" id="headerTitleContainerEl">
                <span class="app-name-text glow-text">App Name</span>
                <small id="headerUserGreetingEl" style="display:none;"></small>
            </div>
            <div class="header-title" id="headerGameTitleEl" style="display:none; line-height: 1.3;" data-i18n="page_title">Page Title</div>
        </div>
        <div class="header-right d-flex align-items-center gap-2 flex-shrink-0">
            <button class="notification-icon bg-transparent border-0 text-main position-relative" id="notificationBtnEl" style="display: none; font-size: 1.4rem; color: var(--text-main);">
                <i class="bi bi-bell drop-shadow glow-text"></i>
                <span class="notification-badge" id="notificationBadgeEl" style="display: none; position:absolute; top:-2px; right:-2px; background:#ef4444; color:white; font-size:0.6rem; width:16px; height:16px; border-radius:50%; align-items:center; justify-content:center; font-weight:bold; box-shadow: 0 0 5px #ef4444;">0</span>
            </button>
            <button class="wallet-chip" id="headerWalletChipEl" style="display: none;" data-section="wallet-section">
                <span class="c-sym me-1" style="display:inline-flex; align-items:center;"></span> <span id="headerChipBalanceEl" style="margin-top:1px;">0</span>
            </button>
        </div>
    </header>

    <main class="main-content">
        <!-- LOGIN / SIGNUP -->
        <section id="login-section" class="section active">
            <div class="text-center mb-4 pt-4">
                <img src="https://via.placeholder.com/100/18181b/06b6d4?text=LOGO" class="app-logo-img" style="width: 80px; height: 80px; object-fit: cover; border-radius: 16px; margin-bottom: 16px; box-shadow: var(--glow-shadow);">
                <h2 class="fw-bold m-0 text-gradient"><span data-i18n="welcome_to">Welcome to</span> <span class="app-name-text">MrBattleZone</span></h2>
            </div>
            
            <form id="emailLoginForm">
                <div class="mb-3"><label class="form-label" data-i18n="email_addr">Email Address</label><input type="email" class="form-control" id="loginEmailInputEl" placeholder="player@email.com" required></div>
                <div class="mb-3"><label class="form-label" data-i18n="password">Password</label><input type="password" class="form-control" id="loginPasswordInputEl" placeholder="••••••••" required></div>
                <button type="button" class="btn-custom btn-primary-gradient mt-2 mb-3" id="loginEmailBtnEl" data-i18n="secure_login">Secure Login</button>
                <button type="button" class="btn-custom btn-outline-custom" id="showSignupToggleBtnEl" data-i18n="create_account">Create New Account</button>
            </form>

            <form id="emailSignupForm" style="display: none;">
                <div class="mb-3"><label class="form-label" data-i18n="in_game_name">In-Game Name</label><input type="text" class="form-control" id="signupNameInputEl" placeholder="Your Game Name" required></div>
                <div class="mb-3"><label class="form-label" data-i18n="email_addr">Email Address</label><input type="email" class="form-control" id="signupEmailInputEl" placeholder="Your Email Id" required></div>
                <div class="mb-3"><label class="form-label" data-i18n="password">Password</label><input type="password" class="form-control" id="signupPasswordInputEl" placeholder="Min 6 characters" required minlength="6"></div>
                <div class="mb-3"><label class="form-label" data-i18n="invite_code_opt">Invite Code (Optional)</label><input type="text" class="form-control" id="signupReferralCodeInputEl" placeholder="Ex: AXPY"></div>
                <button type="button" class="btn-custom btn-primary-gradient mt-2 mb-3" id="signupEmailBtnEl" data-i18n="register_acc">Register Account</button>
                <button type="button" class="btn-custom btn-outline-custom" id="showLoginToggleBtnEl" data-i18n="back_login">Back to Login</button>
            </form>
        </section>

        <!-- HOME -->
        <section id="home-section" class="section">
            
            <!-- PREMIUM ANNOUNCEMENT BAR -->
            <div id="announcementBarContainer" style="display: none;">
                <div class="announcement-bar">
                    <i class="bi bi-megaphone-fill announcement-icon"></i>
                    <div class="announcement-marquee">
                        <div class="announcement-text" id="announcementMarqueeText"></div>
                    </div>
                </div>
            </div>

            <!-- Promotions Auto Slider System -->
            <div id="promoSliderContainer" class="mb-4" style="display:none; position:relative; border-radius:var(--radius-md); overflow:hidden; box-shadow:var(--glow-shadow);">
                <div id="promoSliderTrack" style="display:flex; transition: transform 0.5s ease; height: 180px;"></div>
            </div>

            <!-- MY CONTESTS (ONGOING / UPCOMING / RESULTS CARDS) -->
            <h2 class="section-title"><i class="bi bi-shield-check glow-text" style="color: var(--accent-cyan);"></i> <span data-i18n="my_contests">My Contests</span></h2>
            <div class="my-contests-grid" id="myContestsQuickGrid">
                <div class="contest-status-card ongoing-card" data-contest-status="ongoing" role="button" tabindex="0">
                    <i class="bi bi-broadcast"></i>
                    <span class="contest-card-label" data-i18n="ongoing">Ongoing</span>
                </div>
                <div class="contest-status-card upcoming-card" data-contest-status="upcoming" role="button" tabindex="0">
                    <i class="bi bi-clock-fill"></i>
                    <span class="contest-card-label" data-i18n="upcoming">Upcoming</span>
                </div>
                <div class="contest-status-card completed-card" data-contest-status="completed" role="button" tabindex="0">
                    <i class="bi bi-trophy-fill"></i>
                    <span class="contest-card-label" data-i18n="results">Results</span>
                </div>
            </div>

            <h2 class="section-title"><i class="bi bi-lightning-charge-fill" style="color: var(--accent-gold); filter: drop-shadow(0 0 5px var(--accent-gold));"></i> <span data-i18n="top_games">Top Games</span></h2>
            <div class="games-grid mb-4 placeholder-glow" id="gamesListEl">
                <div class="game-card-new placeholder"></div><div class="game-card-new placeholder"></div><div class="game-card-new placeholder"></div>
            </div>
        </section>

        <!-- MY CONTESTS FILTERED SECTION -->
        <section id="my-contests-section" class="section">
            <div class="tournament-tabs" id="myContestsTabsEl">
                <button class="tab-item active" data-status="ongoing" data-i18n="ongoing">Ongoing</button>
                <button class="tab-item" data-status="upcoming" data-i18n="upcoming">Upcoming</button>
                <button class="tab-item" data-status="completed" data-i18n="results">Results</button>
            </div>
            <div id="myContestsListEl" class="placeholder-glow"></div>
            <div id="noContestsMessageEl" class="text-center py-5" style="display: none;">
                <i class="bi bi-emoji-frown text-muted" style="font-size: 3rem;"></i>
                <p class="text-muted fw-bold mt-2" id="noContestsTextEl" data-i18n="no_joined_matches">No matches joined.</p>
            </div>
        </section>

        <!-- MODES SECTION -->
        <section id="modes-section" class="section">
            <div class="modes-grid mb-4" id="modesListEl"></div>
        </section>

        <!-- REFERRAL -->
        <section id="referral-section" class="section">
            <div class="text-center pt-3 mb-4">
                <i class="bi bi-boxes text-gradient" style="font-size: 5rem; filter: drop-shadow(var(--glow-shadow));"></i>
                <h2 class="fw-bold mb-2 mt-2" data-i18n="refer_earn">Refer & Earn</h2>
                <p class="text-muted small px-2">Invite friends to play. You both earn <strong style="color: var(--text-main);" id="referralBonusText">0</strong>!</p>
            </div>

            <div class="referral-stats-container d-flex gap-3 mb-4">
                <div class="glass-card flex-fill text-center p-3 m-0" style="border-color: var(--accent-cyan);">
                    <i class="bi bi-people-fill fs-2 glow-text" style="color: var(--accent-cyan);"></i>
                    <strong class="d-block fs-3 mt-2 text-main" id="referralTotalJoinedEl">0</strong>
                    <span class="small text-muted text-uppercase fw-bold">Friends Invited</span>
                </div>
                <div class="glass-card flex-fill text-center p-3 m-0" style="border-color: var(--accent-gold);">
                    <i class="bi bi-cash-coin fs-2 glow-text" style="color: var(--accent-gold);"></i>
                    <strong class="d-block fs-3 mt-2 text-main" style="color: var(--accent-gold) !important;" id="referralTotalEarnedEl">0</strong>
                    <span class="small text-muted text-uppercase fw-bold">Bonus Earned</span>
                </div>
            </div>

            <div class="glass-card text-center position-relative glowing-card m-0 p-4">
                <div class="particles-bg"></div>
                <p class="text-main small fw-bold mb-3 text-uppercase position-relative z-1" style="letter-spacing: 1px;">Share Your Invite Link</p>
                <div class="p-3 rounded fw-bold fs-6 mb-4 text-truncate position-relative z-1" style="background: rgba(0,0,0,0.4); border: 1px solid var(--border-glass); color: var(--text-muted);" id="myReferralLinkEl">Generating...</div>
                <div class="position-relative z-1">
                    <button class="btn-custom btn-outline-custom w-100 copy-btn btn-hover-glow" data-target="#myReferralLinkEl"><i class="bi bi-link-45deg fs-4"></i> Copy</button>
                </div>
            </div>
        </section>

        <!-- SETTINGS -->
        <section id="settings-section" class="section">
            <div class="text-center pt-3 mb-4">
                <i class="bi bi-gear text-gradient" style="font-size: 4rem; filter: drop-shadow(var(--glow-shadow));"></i>
                <h2 class="fw-bold mb-2 mt-2" data-i18n="settings">Settings</h2>
            </div>
            
            <!-- Light & Dark Mode Feature -->
            <div class="glass-card mb-4">
                <h6 class="text-muted text-uppercase fw-bold mb-3 small">Light & Dark Mode</h6>
                <div class="d-flex gap-2">
                    <button class="btn btn-outline-custom flex-fill fw-bold theme-mode-btn btn-hover-glow" data-theme="theme-light"><i class="bi bi-sun-fill text-warning"></i> Light Mode</button>
                    <button class="btn btn-outline-custom flex-fill fw-bold theme-mode-btn btn-hover-glow" data-theme="theme-dark"><i class="bi bi-moon-stars-fill text-info"></i> Dark Mode</button>
                </div>
            </div>

            <div class="glass-card mb-4">
                <h6 class="text-muted text-uppercase fw-bold mb-3 small" data-i18n="language">Language</h6>
                <div class="d-flex gap-2">
                    <button class="btn btn-outline-custom flex-fill fw-bold lang-toggle-btn btn-hover-glow" data-lang="en">English</button>
                    <button class="btn btn-outline-custom flex-fill fw-bold lang-toggle-btn btn-hover-glow" data-lang="hi">हिंदी</button>
                </div>
            </div>

            <div class="glass-card" id="themeSelectionContainer">
                <div class="d-flex justify-content-between align-items-center mb-3">
                    <h6 class="text-muted text-uppercase fw-bold m-0 small" data-i18n="select_theme">Select Premium Theme</h6>
                    <button class="btn btn-sm btn-outline-custom" id="useAdminThemeBtn" style="font-size: 0.75rem; padding: 4px 10px; border-radius: 8px;">
                        <i class="bi bi-arrow-clockwise text-info"></i> <span data-i18n="use_admin_theme">Use Admin Theme</span>
                    </button>
                </div>
                <div class="theme-grid">
                    <div class="theme-card-select" data-theme="theme-neon"><div class="theme-indicator" style="background: #000; border-color: #39ff14;"><i class="bi bi-lightning-charge-fill" style="color: #39ff14;"></i></div><strong class="d-block small">Neon Green</strong></div>
                    <div class="theme-card-select" data-theme="theme-cyber"><div class="theme-indicator" style="background: #0b1120; border-color: #0ea5e9;"><i class="bi bi-cpu-fill" style="color: #0ea5e9;"></i></div><strong class="d-block small">Cyber Blue</strong></div>
                    <div class="theme-card-select" data-theme="theme-purple"><div class="theme-indicator" style="background: #200042; border-color: #a855f7;"><i class="bi bi-stars" style="color: #a855f7;"></i></div><strong class="d-block small">Purple Galaxy</strong></div>
                    <div class="theme-card-select" data-theme="theme-red"><div class="theme-indicator" style="background: #2e0808; border-color: #ef4444;"><i class="bi bi-fire" style="color: #ef4444;"></i></div><strong class="d-block small">Red Dragon</strong></div>
                    <div class="theme-card-select" data-theme="theme-gold"><div class="theme-indicator" style="background: #292524; border-color: #eab308;"><i class="bi bi-gem" style="color: #eab308;"></i></div><strong class="d-block small">Gold Royal</strong></div>
                </div>
            </div>
        </section>
        
        <!-- TOURNAMENTS -->
        <section id="tournaments-section" class="section">
            <div class="tournament-tabs" id="tournamentsTabsEl"> 
                <button class="tab-item active" data-status="upcoming" data-i18n="upcoming">Upcoming</button> 
                <button class="tab-item" data-status="ongoing" data-i18n="ongoing">Ongoing</button> 
                <button class="tab-item" data-status="completed" data-i18n="results">Results</button> 
            </div>
            <div id="tournamentsListContainerEl" class="placeholder-glow"></div>
            <div id="noTournamentsMessageEl" class="text-center py-5" style="display: none;"><i class="bi bi-emoji-frown text-muted" style="font-size: 3rem;"></i><p class="text-muted fw-bold mt-2" data-i18n="no_matches_sched">No matches scheduled.</p></div>
        </section>

        <!-- WALLET -->
        <section id="wallet-section" class="section">
            <h2 class="section-title mb-3" data-i18n="wallet">Wallet</h2>
            <div class="glass-card mb-4" style="background: var(--gradient-primary); text-align: center;">
                <div class="balance-label text-white text-uppercase small fw-bold" data-i18n="total_balance">Total Balance</div>
                <div class="balance-value text-white fw-bold fs-1 my-2 d-flex justify-content-center align-items-center placeholder-glow" id="walletTotalBalanceContainer"><span class="placeholder col-4" id="walletTotalBalanceEl"></span></div>
                <div class="d-flex gap-2">
                    <button class="btn-custom btn-outline-custom flex-fill text-white btn-hover-glow" style="border-color: rgba(255,255,255,0.3); background: rgba(0,0,0,0.2);" id="addAmountWalletBtnEl"><i class="bi bi-plus-lg"></i> <span data-i18n="deposit">Deposit</span></button>
                    <button class="btn-custom btn-outline-custom flex-fill text-white btn-hover-glow" style="border-color: rgba(255,255,255,0.3); background: rgba(0,0,0,0.2);" id="withdrawBtnEl"><i class="bi bi-arrow-down-left"></i> <span data-i18n="withdraw">Withdraw</span></button>
                </div>
            </div>
            
            <div class="row g-3 mb-4 placeholder-glow" id="walletSplitContainer">
                <div class="col-6"><div class="glass-card text-center p-3 m-0"><i class="bi bi-trophy-fill fs-3 mb-2 d-block glow-text" style="color: var(--accent-gold);"></i><span class="small text-muted fw-bold text-uppercase d-block mb-1" data-i18n="winnings">Winnings</span><h4 class="mb-0 fw-bold d-flex justify-content-center align-items-center text-main" id="walletWinningCashContainer"><span class="placeholder col-6" id="walletWinningCashEl"></span></h4></div></div>
                <div class="col-6"><div class="glass-card text-center p-3 m-0"><i class="bi bi-gift-fill fs-3 mb-2 d-block glow-text" style="color: var(--accent-cyan);"></i><span class="small text-muted fw-bold text-uppercase d-block mb-1" data-i18n="bonus">Bonus</span><h4 class="mb-0 fw-bold d-flex justify-content-center align-items-center text-main" id="walletBonusCashContainer"><span class="placeholder col-6" id="walletBonusCashEl"></span></h4></div></div>
            </div>

            <div class="glass-card p-3 mb-4">
                <h6 class="text-uppercase fw-bold text-muted small mb-2" data-i18n="redeem_code">Redeem Code</h6>
                <div class="d-flex gap-2">
                    <input type="text" class="form-control text-uppercase" style="letter-spacing: 2px; font-weight: bold;" id="redeemCodeInput" placeholder="Enter Gift Code">
                    <button class="btn btn-primary-gradient px-3 fw-bold rounded-3 text-white border-0" id="applyRedeemBtnEl" data-i18n="apply">Apply</button>
                </div>
            </div>

            <div class="d-flex justify-content-between align-items-center mt-4 mb-3">
                <h2 class="section-title m-0"><i class="bi bi-clock-history glow-text" style="color: var(--accent-purple);"></i> <span data-i18n="txn_history">History</span></h2>
                <button class="btn btn-sm btn-outline-custom fw-bold" data-bs-toggle="modal" data-bs-target="#orderStatusModalEl" style="font-size: 0.75rem;"><i class="bi bi-search"></i> Check Status</button>
            </div>
            <div id="walletHistoryListEl" class="placeholder-glow mb-4"></div>
        </section>

        <!-- RECHARGE -->
        <section id="recharge-section" class="section">
            <div id="recharge-step-1-amount">
                <h2 class="section-title text-center mb-3 pt-2 justify-content-center" data-i18n="add_funds">Add Funds</h2>
                <div class="glass-card text-center py-4">
                    <label class="form-label d-block mb-3" id="rechargeLimitLabelEl">Enter Amount</label>
                    <div class="d-flex justify-content-center align-items-center mb-4">
                        <span class="fw-bold text-muted me-1 c-sym" style="font-size: 2rem;"></span>
                        <input type="number" id="rechargeAmountInput" class="form-control text-center fw-bold" style="background: transparent; border: none; border-bottom: 2px solid var(--accent-cyan); border-radius: 0; width: 120px; font-size: 2.5rem; padding: 0;" placeholder="0">
                    </div>
                    <div class="d-flex flex-wrap justify-content-center gap-2 mb-4">
                        <button class="btn btn-outline-custom amount-preset-btn rounded-pill px-3 py-1 fw-bold small" data-amount="50"><span class="c-sym"></span>50</button>
                        <button class="btn btn-outline-custom amount-preset-btn rounded-pill px-3 py-1 fw-bold small" data-amount="100"><span class="c-sym"></span>100</button>
                        <button class="btn btn-outline-custom amount-preset-btn rounded-pill px-3 py-1 fw-bold small" data-amount="200"><span class="c-sym"></span>200</button>
                        <button class="btn btn-outline-custom amount-preset-btn rounded-pill px-3 py-1 fw-bold small" data-amount="500"><span class="c-sym"></span>500</button>
                    </div>
                    <button class="btn-custom btn-primary-gradient w-100" id="goToStep2Btn" data-i18n="next_step">Next Step</button>
                </div>
            </div>
            <div id="recharge-step-2-method" style="display: none;">
                <h2 class="section-title text-center mb-3 pt-2 justify-content-center" data-i18n="select_pay_mode">Select Payment Mode</h2>
                <div class="glass-card text-center">
                    <span class="text-muted fw-bold text-uppercase small">Adding</span>
                    <h3 class="fw-bold m-0 mb-4 text-gradient d-flex justify-content-center align-items-center"><span class="c-sym"></span><span id="rechargeAmountConfirm">0</span></h3>
                    <div class="text-start mb-4">
                        <label class="glass-card d-flex align-items-center justify-content-between p-3 m-0 mb-3 cursor-pointer" style="border-radius:var(--radius-md);" id="optionAutoCard">
                            <div class="d-flex align-items-center gap-3">
                                <i class="bi bi-lightning-charge-fill fs-3 glow-text" style="color: var(--accent-cyan);"></i>
                                <div><strong class="d-block text-main">Auto Payment</strong><span class="small text-muted">ZapUPI Instant</span></div>
                            </div>
                            <input type="radio" name="payType" value="auto" style="transform: scale(1.3); accent-color: var(--accent-cyan);">
                        </label>
                        <label class="glass-card d-flex align-items-center justify-content-between p-3 m-0 cursor-pointer" style="border-radius:var(--radius-md);" id="optionManualCard">
                            <div class="d-flex align-items-center gap-3">
                                <i class="bi bi-qr-code-scan fs-3 glow-text" style="color: var(--accent-purple);"></i>
                                <div><strong class="d-block text-main">Manual Transfer</strong><span class="small text-muted">Scan QR & Submit UTR</span></div>
                            </div>
                            <input type="radio" name="payType" value="manual" style="transform: scale(1.3); accent-color: var(--accent-cyan);">
                        </label>
                    </div>
                    <button class="btn-custom btn-primary-gradient w-100" id="proceedToPayActionBtn" data-i18n="proceed_pay">Proceed to Pay</button>
                </div>
            </div>
            <div id="recharge-step-3-manual" style="display: none;">
                <h2 class="section-title text-center mb-3 pt-2 justify-content-center" data-i18n="manual_pay">Manual Payment</h2>
                <div class="glass-card text-center">
                    <p class="text-muted small mb-3">Scan QR or Copy UPI ID to pay exactly <strong style="color: var(--text-main);" class="fs-5 d-inline-flex align-items-center"><span class="c-sym"></span><span id="rechargeFinalAmount">0</span></strong></p>
                    <div class="bg-white p-2 rounded-3 d-inline-block mb-3 shadow-lg"><img src="https://via.placeholder.com/150" id="rechargeQrCodeImg" style="width:160px; height:160px; object-fit:contain;"></div>
                    <div class="p-3 rounded-3 mb-4 d-flex justify-content-between align-items-center" style="background: rgba(128,128,128,0.1); border: 1px solid var(--border-glass);">
                        <div class="text-start"><span class="small text-muted d-block fw-bold mb-1">Target UPI ID</span><strong style="color: var(--text-main);" class="fs-6" id="rechargeUpiId">admin@upi</strong></div>
                        <button class="btn btn-sm btn-outline-custom copy-btn" data-target="#rechargeUpiId"><i class="bi bi-clipboard"></i></button>
                    </div>
                    <h6 class="fw-bold text-start mb-2 small text-muted text-uppercase">Submit UTR (Ref No)</h6>
                    <input type="text" class="form-control mb-3" id="rechargeUtrInput" placeholder="Enter 12-digit UTR">
                    <button class="btn-custom btn-primary-gradient w-100" id="rechargeSubmitBtn" data-i18n="verify_transfer">Verify Transfer</button>
                </div>
            </div>
        </section>

        <!-- PROFILE -->
        <section id="profile-section" class="section">
            <div class="glass-card profile-header border-0 shadow-none mb-0 bg-transparent text-center">
                <div class="profile-avatar-wrapper position-relative d-inline-block mb-3 placeholder-glow" id="profileAvatarContainer">
                    <img src="https://via.placeholder.com/100" class="profile-avatar placeholder" style="width: 90px; height: 90px; border-radius: 50%; border: 3px solid var(--accent-purple); object-fit: cover; padding: 3px; background: var(--bg-card); box-shadow: var(--glow-shadow);" id="profileAvatarEl">
                    <button class="edit-avatar-btn d-none" id="editNameBtnEl" style="position:absolute; bottom:0; right:0; background:var(--accent-cyan); border:none; border-radius:50%; width:30px; height:30px; color:white; box-shadow: 0 0 10px var(--accent-cyan);"><i class="bi bi-pencil-fill"></i></button>
                </div>
                <h3 class="fw-bold m-0 mt-2 mb-1 placeholder-glow"><span class="placeholder col-6" id="profileNameEl"></span></h3>
                <p class="text-muted small mb-0 placeholder-glow"><span class="placeholder col-8" id="profileEmailEl"></span></p>
                <div class="d-none" id="profileUidEl"></div>
                <p class="text-info font-monospace small mb-4 mt-1" style="font-size: 0.8rem;"><span id="profileRefCodeEl" style="background: rgba(6, 182, 212, 0.1); padding: 4px 10px; border-radius: 8px; border: 1px solid var(--accent-cyan);"></span></p>
                
                <div class="row g-2 profile-stats-grid placeholder-glow mb-4" id="profileStatsGridContainer">
                    <div class="col-4"><div class="glass-card text-center p-2 m-0 border-0"><strong class="fs-4"><span class="placeholder col-6" id="profileTotalMatchesEl"></span></strong><span class="d-block small text-muted text-uppercase fw-bold" data-i18n="matches">Matches</span></div></div>
                    <div class="col-4"><div class="glass-card text-center p-2 m-0 border-0"><strong class="fs-4"><span class="placeholder col-6" id="profileWonMatchesEl"></span></strong><span class="d-block small text-muted text-uppercase fw-bold" data-i18n="wins">Wins</span></div></div>
                    <div class="col-4"><div class="glass-card text-center p-2 m-0 border-0 d-flex flex-column align-items-center"><strong style="color: var(--accent-gold);" class="fs-4 d-flex align-items-center"><span class="placeholder col-8" id="profileTotalEarningsEl"></span></strong><span class="d-block small text-muted text-uppercase fw-bold" data-i18n="earned">Earn</span></div></div>
                </div>
            </div>

            <div class="glass-card p-3 mb-4">
                <h6 class="text-uppercase fw-bold text-muted small mb-2" data-i18n="apply_coupon">Apply Promo Coupon</h6>
                <div class="d-flex gap-2">
                    <input type="text" class="form-control text-uppercase" id="couponCodeInput" placeholder="Enter Coupon Code" style="letter-spacing: 1px;">
                    <button class="btn btn-primary-gradient px-3 fw-bold rounded-3 text-white border-0" id="applyCouponBtnEl" data-i18n="apply">Apply</button>
                </div>
            </div>

            <div class="list-group glass-card p-0 overflow-hidden mb-4">
                <a href="#" class="list-group-item" data-section="matchhistory-trigger"><div><i class="bi bi-clock-history"></i> <span data-i18n="match_history">Match History</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <a href="#" class="list-group-item" data-section="tutorials-section"><div><i class="bi bi-play-circle-fill"></i> <span data-i18n="app_tutorial">App Tutorials</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <a href="#" class="list-group-item" data-section="referral-section"><div><i class="bi bi-gift-fill"></i> <span data-i18n="refer_earn">Refer & Earn</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <a href="#" class="list-group-item" data-section="settings-section"><div><i class="bi bi-gear-fill"></i> <span data-i18n="settings">Settings</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <a href="#" class="list-group-item" data-section="support-section"><div><i class="bi bi-headset"></i> <span data-i18n="help_support">Help & Support</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <a href="#" class="list-group-item" data-section="policies-section"><div><i class="bi bi-shield-check"></i> <span data-i18n="rules_policies">Rules & Policies</span></div><i class="bi bi-chevron-right text-muted"></i></a>
                <button class="list-group-item text-danger w-100 text-start" id="logoutProfileBtnEl" style="display:block;"><i class="bi bi-box-arrow-right" style="filter: drop-shadow(0 0 5px #ef4444); color: #ef4444;"></i> <span data-i18n="logout">Secure Logout</span></button>
            </div>
        </section>

        <!-- OTHERS -->
        <section id="tutorials-section" class="section">
            <h2 class="section-title text-center justify-content-center pt-3 mb-4" data-i18n="app_tutorial">App Tutorials</h2>
            <div id="tutorialsListEl" class="placeholder-glow"></div>
            <p id="noTutorialsMsg" class="text-center text-muted small mt-4 fw-bold" style="display:none;" data-i18n="no_tutorials">No tutorials available.</p>
        </section>

        <section id="leaderboard-section" class="section">
            <div class="text-center mb-4 mt-2">
                <i class="bi bi-trophy-fill glow-text" style="font-size: 4rem; color: var(--accent-gold);"></i>
                <h2 class="section-title justify-content-center m-0 mt-3" data-i18n="hall_fame">Hall of Fame</h2>
            </div>
            <div class="glass-card p-2" id="leaderboardListEl"></div>
        </section>

        <section id="earnings-section" class="section">
            <h2 class="section-title" data-i18n="stats">Statistics & Earnings</h2>
            <div class="glass-card text-center py-4 mb-3 placeholder-glow" id="earningsTotalContainer">
                <div style="width: 60px; height: 60px; background: rgba(6, 182, 212, 0.1); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; box-shadow: var(--glow-shadow);"><i class="bi bi-graph-up-arrow fs-2 glow-text" style="color: var(--accent-cyan);"></i></div>
                <h2 class="fw-bold mb-1 d-flex justify-content-center align-items-center text-main"><span class="placeholder col-4" id="earningsTotalEl"></span></h2>
                <p class="text-muted small text-uppercase fw-bold m-0" data-i18n="match_earn">Match Earnings</p>
            </div>
            <div class="glass-card text-center py-4 placeholder-glow" id="earningsReferralContainer">
                <div style="width: 60px; height: 60px; background: rgba(139, 92, 246, 0.1); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; box-shadow: var(--glow-shadow);"><i class="bi bi-people-fill fs-2 glow-text" style="color: var(--accent-purple);"></i></div>
                <h2 class="fw-bold mb-1 d-flex justify-content-center align-items-center text-main"><span class="placeholder col-4" id="earningsReferralEl"></span></h2>
                <p class="text-muted small text-uppercase fw-bold m-0" data-i18n="refer_reward">Referral Rewards</p>
            </div>
        </section>

        <section id="support-section" class="section">
            <div class="text-center pt-3 mb-4">
                <i class="bi bi-headset glow-text" style="font-size: 4rem; color: var(--accent-purple);"></i>
                <h2 class="fw-bold mb-2 mt-2" data-i18n="support">Support</h2>
            </div>
            <div class="px-2" id="supportLinksContainer">
                <a href="#" class="btn-custom mb-3 btn-hover-glow" id="supportWaBtn" target="_blank" style="display:none; background: #25D366; color:white; border-radius: 16px;"><i class="bi bi-whatsapp fs-4"></i> WhatsApp Support</a>
                <a href="#" class="btn-custom mb-3 btn-hover-glow" id="supportTgBtn" target="_blank" style="display:none; background: #0088cc; color:white; border-radius: 16px;"><i class="bi bi-telegram fs-4"></i> Join Telegram</a>
                <p id="noSupportLinksMsg" class="text-center text-muted small mt-4" style="display:none;">Support options are currently unavailable.</p>
            </div>
        </section>

        <section id="policies-section" class="section">
            <h2 class="section-title justify-content-center mb-4" data-i18n="rules_policies">Rules & Policies</h2>
            <div class="accordion premium-accordion" id="policiesAccordion"></div>
        </section>
    </main>

    <!-- FULL SCREEN NOTIFICATION OVERLAY -->
    <div id="notificationOverlay" class="notification-overlay">
        <div class="notification-header">
            <button id="closeNotification"><i class="bi bi-arrow-left-short glow-text" style="font-size: 2rem;"></i></button>
            <h3>Notifications</h3>
            <div style="width: 32px;"></div>
        </div>
        <div id="notificationsListEl" class="notification-list"></div>
        <p id="notificationsEmptyMsgEl" class="text-center text-muted py-5 fw-bold" style="display: none; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%;">No Notifications Available</p>
    </div>

    <!-- Bottom Navigation -->
    <nav class="bottom-nav">
        <button class="nav-item active" data-section="home-section"><i class="bi bi-house-door-fill"></i><span data-i18n="home">Home</span></button>
        <button class="nav-item" data-section="wallet-section"><i class="bi bi-wallet2"></i><span data-i18n="wallet">Wallet</span></button>
        <button class="nav-item nav-item-center" data-section="leaderboard-section"><i class="bi bi-trophy-fill"></i><span>Rank</span></button>
        <button class="nav-item" data-section="earnings-section"><i class="bi bi-graph-up-arrow"></i><span data-i18n="stats">Stats</span></button>
        <button class="nav-item" data-section="profile-section"><i class="bi bi-person-fill"></i><span data-i18n="profile">Profile</span></button>
    </nav>

    <!-- MODALS -->
    <!-- Prize List Modal -->
    <div class="modal fade" id="prizeListModalEl" tabindex="-1"><div class="modal-dialog modal-dialog-centered modal-sm"><div class="modal-content"><div class="modal-header border-bottom" style="border-color: var(--border-glass) !important;"><h5 class="modal-title fw-bold text-gradient"><i class="bi bi-trophy-fill text-warning me-2"></i> Prize Pool</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body p-0" id="prizeListModalBodyEl"></div></div></div></div>

    <div class="modal fade" id="orderStatusModalEl" tabindex="-1"><div class="modal-dialog modal-dialog-centered"><div class="modal-content"><div class="modal-header"><h5 class="modal-title"><i class="bi bi-shield-check text-info me-2"></i> Payment Status</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body text-center"><div class="mb-3 text-start"><label class="form-label">Order ID</label><input type="text" class="form-control" id="statusCheckOrderId" placeholder="ORD1710000000000"></div><button type="button" class="btn-custom btn-primary-gradient w-100 mb-4" id="checkZapStatusBtn">Verify Status</button><div id="statusCheckResult" class="glass-card text-start p-3 text-main" style="display:none; font-size: 0.85rem;"></div></div></div></div></div>
    <div class="modal fade" id="withdrawModalEl" tabindex="-1"><div class="modal-dialog modal-dialog-centered"><div class="modal-content"><div class="modal-header"><h5 class="modal-title"><i class="bi bi-bank me-2" style="color:var(--accent-cyan);"></i> Withdraw Funds</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body"><div class="glass-card text-center mb-3 p-3"><span class="small text-muted fw-bold text-uppercase">Available Winnings</span><h3 style="color: var(--text-main);" class="fw-bold m-0 mt-1 d-flex justify-content-center align-items-center" id="withdrawModalBalanceEl">0.00</h3></div><div class="d-flex p-1 rounded-pill mb-3" style="background: rgba(128,128,128,0.1); border: 1px solid var(--border-glass);"><button class="btn flex-fill rounded-pill fw-bold active wd-tab-btn" data-type="money" style="background: var(--bg-card); color: var(--text-main);">Money Transfer</button><button class="btn flex-fill rounded-pill fw-bold text-muted wd-tab-btn" data-type="redeem">Redeem Code</button></div><div id="wdMoneySection"><div class="mb-3"><label class="form-label">Amount (Min <span class="c-sym"></span><span id="minWithdrawAmountEl">50</span>)</label><input type="number" class="form-control" id="withdrawAmountInputEl" placeholder="Enter amount"></div><div class="mb-4"><label class="form-label">Payment Method (UPI/Bank)</label><input type="text" class="form-control" id="withdrawMethodInputEl" placeholder="Enter UPI ID or Bank Details"></div></div><div id="wdRedeemSection" style="display:none;"><div class="p-2 rounded mb-3" style="background: rgba(6, 182, 212, 0.1); border: 1px solid var(--accent-cyan);"><p class="text-muted small m-0 fw-bold"><i class="bi bi-info-circle text-cyan"></i> Request a Play Store / Game Redeem Code. Balance is securely held pending admin approval.</p></div><div class="mb-4"><label class="form-label">Amount (Min <span class="c-sym"></span><span id="minRedeemAmountEl">50</span>)</label><input type="number" class="form-control" id="withdrawRedeemAmountInputEl" placeholder="Enter redeem amount"></div></div><button type="button" class="btn-custom btn-primary-gradient w-100" id="submitWithdrawRequestBtnEl">Submit Request</button></div></div></div></div>
    <div class="modal fade" id="editNameModal" tabindex="-1"><div class="modal-dialog modal-dialog-centered"><div class="modal-content"><div class="modal-header"><h5 class="modal-title">Edit Profile</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body"><div class="mb-3"><label class="form-label">Display Name</label><input type="text" class="form-control" id="editNameInput" required></div><hr class="my-3 border-secondary"><div class="mb-3"><label class="form-label">New Password (Optional)</label><input type="password" class="form-control" id="editPasswordInput" placeholder="Leave blank to keep current"></div><button type="button" class="btn-custom btn-primary-gradient w-100 mt-2" id="saveNameChangeBtn">Save Changes</button></div></div></div></div>
    <div class="modal fade" id="matchHistoryModal" tabindex="-1"><div class="modal-dialog modal-dialog-centered modal-dialog-scrollable"><div class="modal-content" style="height: 80vh;"><div class="modal-header"><h5 class="modal-title"><i class="bi bi-clock-history me-2" style="color:var(--accent-cyan);"></i> Match History</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body" id="matchHistoryBodyEl"></div></div></div></div>
    <div class="modal fade" id="matchDetailsModalEl" tabindex="-1"><div class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-lg"><div class="modal-content"><div class="modal-header"><h5 class="modal-title" id="matchDetailsModalTitleEl">Match Details</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body text-muted" id="matchDetailsModalBodyEl" style="line-height: 1.6;"></div></div></div></div>
    
    <!-- Dynamic Join Match Modal -->
    <div class="modal fade" id="joinTournamentDetailsModal" tabindex="-1"><div class="modal-dialog modal-dialog-centered modal-dialog-scrollable"><div class="modal-content"><div class="modal-header"><h5 class="modal-title text-gradient">Join Match</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body"><div class="glass-card text-center mb-3 p-3"><span class="text-muted small fw-bold text-uppercase">Total Entry Fee</span><h3 id="joinFeeDisplayEl" style="color: var(--text-main);" class="fw-bold m-0 mt-1 glow-text d-flex justify-content-center align-items-center">0.00</h3></div><form id="joinTournamentForm"><input type="hidden" id="joinTournamentIdInput"><div id="dynamicPlayerInputsContainer"></div><button type="button" class="btn-custom btn-primary-gradient w-100 mt-2" id="confirmJoinBtn">Confirm & Pay</button></form></div></div></div></div>
    
    <div class="modal fade" id="idPasswordModalEl" tabindex="-1"><div class="modal-dialog modal-dialog-centered"><div class="modal-content"><div class="modal-header"><h5 class="modal-title"><i class="bi bi-key-fill me-2" style="color:var(--accent-gold);"></i> Room Credentials</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button></div><div class="modal-body text-center"><p class="small text-muted mb-4">Credentials will be visible here before match starts.</p><div class="p-3 rounded-3 mb-3 d-flex justify-content-between align-items-center border border-secondary" style="background: rgba(128,128,128,0.1);"><div class="text-start"><span class="small text-muted d-block text-uppercase fw-bold">Room ID</span><strong style="color: var(--text-main);" class="fs-5" id="roomIdDisplayEl">Waiting...</strong></div><button class="btn btn-sm btn-outline-custom copy-btn" data-target="#roomIdDisplayEl"><i class="bi bi-clipboard"></i></button></div><div class="p-3 rounded-3 mb-4 d-flex justify-content-between align-items-center border border-secondary" style="background: rgba(128,128,128,0.1);"><div class="text-start"><span class="small text-muted d-block text-uppercase fw-bold">Password</span><strong style="color: var(--text-main);" class="fs-5" id="roomPasswordDisplayEl">Waiting...</strong></div><button class="btn btn-sm btn-outline-custom copy-btn" data-target="#roomPasswordDisplayEl"><i class="bi bi-clipboard"></i></button></div></div></div></div></div>

    <!-- Firebase & Logic Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-app.js";
        import { getDatabase, ref, get, set, update, push, query, orderByChild, equalTo, onValue, off, serverTimestamp, runTransaction } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-database.js";
        import { getAuth, signOut, onAuthStateChanged, createUserWithEmailAndPassword, signInWithEmailAndPassword, updatePassword } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-auth.js";

        const firebaseConfig = {
  apiKey: "AIzaSyAh2DcOlcGalgn8T81mkC5nV2FTm2Pe_mg",
  authDomain: "tournament-ce837.firebaseapp.com",
  databaseURL: "https://tournament-ce837-default-rtdb.firebaseio.com",
  projectId: "tournament-ce837",
  storageBucket: "tournament-ce837.firebasestorage.app",
  messagingSenderId: "327471948270",
  appId: "1:327471948270:web:27323c935c6479d37aeeff",
  measurementId: "G-RT3N2SFS3F"
};

        const app = initializeApp(firebaseConfig);
        const db = getDatabase(app);
        const auth = getAuth(app);
        const getEl = (id) => document.getElementById(id) || { value:'', innerHTML:'', textContent:'', style:{}, classList:{add:()=>{},remove:()=>{},toggle:()=>{}}, checked:false, dataset:{} };

        let currentUser = null, userProfile = {}, currentSectionId = 'login-section', appSettings = {};
        let currentTournamentGameId = null, currentTournamentModeId = null;
        let currentMyContestStatus = 'ongoing';
        let allGames = {};
        let allModes = {};
        let allTournamentsData = {}; 
        let modals = {};

        // Real-time Trackers
        let activeUserListener = null;
        let activeDepositsListener = null;
        let activeWithdrawalsListener = null;
        let activeReferralsListener = null;
        let activeTournamentsListener = null;
        let activeUserNotifsListener = null;
        let activeGlobalNotifsListener = null;
        let globalThemeLock = false;
        let currentAdminTheme = 'theme-neon';
        let userTxns = [];
        let fetchedNotifs = [];

        function clearUserListeners() {
            if(activeUserListener) { off(activeUserListener.ref, 'value', activeUserListener.callback); activeUserListener = null; }
            if(activeDepositsListener) { off(activeDepositsListener.ref, 'value', activeDepositsListener.callback); activeDepositsListener = null; }
            if(activeWithdrawalsListener) { off(activeWithdrawalsListener.ref, 'value', activeWithdrawalsListener.callback); activeWithdrawalsListener = null; }
            if(activeReferralsListener) { off(activeReferralsListener.ref, 'value', activeReferralsListener.callback); activeReferralsListener = null; }
            if(activeTournamentsListener) { off(activeTournamentsListener.ref, 'value', activeTournamentsListener.callback); activeTournamentsListener = null; }
            if(activeUserNotifsListener) { off(activeUserNotifsListener.ref, 'value', activeUserNotifsListener.callback); activeUserNotifsListener = null; }
            if(activeGlobalNotifsListener) { off(activeGlobalNotifsListener.ref, 'value', activeGlobalNotifsListener.callback); activeGlobalNotifsListener = null; }
        }

        const safeStr = (str, def = 'N/A') => (str === null || str === undefined || String(str).trim() === '') ? def : str;

        const clearPlaceholders = (elId, containerId) => {
            const el = document.getElementById(elId);
            if(el) {
                el.classList.remove('placeholder', 'placeholder-glow', 'col-4', 'col-6', 'col-8', 'col-12');
                const parent = containerId ? document.getElementById(containerId) : el.parentElement;
                if(parent && parent.classList.contains('placeholder-glow')) {
                    parent.classList.remove('placeholder-glow');
                }
            }
        };

        onValue(ref(db, '.info/connected'), (snap) => {
            if (snap.val() === false && currentUser) {
                showToast("Connection lost. Checking network...", "error");
            }
        });

        // ================= GLOBAL CURRENCY SYSTEM =================
        window.FMT_C = (v) => {
            if(v === undefined || v === null || (typeof v === 'number' && isNaN(v))) return '0';
            let strV = String(v).trim();
            if (strV === '' || strV === 'NaN') strV = '0';
            let hasSymbol = /[^\d.,\s\-]/.test(strV); 
            if (hasSymbol) return strV;
            let valStr = Number(strV);
            if(isNaN(valStr)) valStr = 0;
            valStr = (valStr % 1 !== 0) ? valStr.toFixed(2) : valStr.toString();
            const iconUrl = appSettings.currencyIconUrl || appSettings.currencyImage;
            const sym = iconUrl ? `<img src="${iconUrl}" style="width:20px;height:20px;vertical-align:middle;margin-top:-2px;margin-right:4px;display:inline-block;border-radius:50%;object-fit:contain;">` : '₹';
            return `${sym}${valStr}`;
        };

        const applyCurrencySymbol = () => {
            const iconUrl = appSettings.currencyIconUrl || appSettings.currencyImage;
            const symHtml = iconUrl ? `<img src="${iconUrl}" style="width:20px;height:20px;vertical-align:middle;margin-top:-2px;margin-right:4px;display:inline-block;border-radius:50%;object-fit:contain;">` : '₹';
            document.querySelectorAll('.c-sym').forEach(el => el.innerHTML = symHtml);
        };

        // ================= TRANSLATION SYSTEM =================
        const translations = {
            en: { home: "Home", wallet: "Wallet", rank: "Rank", stats: "Stats", profile: "Profile", matches: "Matches", support: "Support", welcome_to: "Welcome to", play_compete_win: "Play. Compete. Win Cash.", email_addr: "Email Address", password: "Password", secure_login: "Secure Login", create_account: "Create New Account", in_game_name: "In-Game Name", invite_code_opt: "Invite Code (Optional)", register_acc: "Register Account", back_login: "Back to Login", top_games: "Top Games", my_contests: "My Contests", no_joined_matches: "No matches joined.", no_ongoing_matches: "No ongoing matches joined.", no_upcoming_matches: "No upcoming matches joined.", no_completed_matches: "No completed matches found.", upcoming: "Upcoming", ongoing: "Ongoing", results: "Results", no_matches_sched: "No matches scheduled.", total_balance: "Total Balance", deposit: "Deposit", withdraw: "Withdraw", winnings: "Winnings", bonus: "Bonus", redeem_code: "Redeem Code", apply: "Apply", txn_history: "History", add_funds: "Add Funds", next_step: "Next Step", select_pay_mode: "Select Payment Mode", proceed_pay: "Proceed to Pay", manual_pay: "Manual Payment", verify_transfer: "Verify Transfer", earned: "Earned", wins: "Wins", apply_coupon: "Apply Promo Coupon", match_history: "Match History", app_tutorial: "App Tutorials", refer_earn: "Refer & Earn", settings: "Settings", help_support: "Help & Support", rules_policies: "Rules & Policies", logout: "Secure Logout", no_tutorials: "No tutorials available.", language: "Language", select_theme: "Select Premium Theme", use_admin_theme: "Use Admin Theme", hall_fame: "Hall of Fame", match_earn: "Match Earnings", refer_reward: "Referral Rewards", loading: "Loading...", select_mode: "Select Mode" },
            hi: { home: "होम", wallet: "वॉलेट", rank: "रैंक", stats: "आंकड़े", profile: "प्रोफ़ाइल", matches: "मैच", support: "सहायता", welcome_to: "स्वागत है", play_compete_win: "खेलें। मुकाबला करें। जीतें।", email_addr: "ईमेल पता", password: "पासवर्ड", secure_login: "लॉगिन करें", create_account: "नया खाता बनाएँ", in_game_name: "गेम का नाम", invite_code_opt: "इनवाइट कोड (वैकल्पिक)", register_acc: "खाता बनाएँ", back_login: "लॉगिन पर वापस", top_games: "शीर्ष खेल", my_contests: "मेरे मैच", no_joined_matches: "कोई मैच नहीं जोड़ा गया।", no_ongoing_matches: "कोई चल रहा मैच नहीं है।", no_upcoming_matches: "कोई आगामी मैच नहीं जोड़ा गया।", no_completed_matches: "कोई पूरा हुआ मैच नहीं है।", upcoming: "आगामी", ongoing: "चल रहे", results: "परिणाम", no_matches_sched: "कोई मैच निर्धारित नहीं है।", total_balance: "कुल राशि", deposit: "जमा करें", withdraw: "निकासी", winnings: "जीती राशि", bonus: "बोनस", redeem_code: "रिडीम कोड", apply: "लागू करें", txn_history: "इतिहास", add_funds: "पैसे जोड़ें", next_step: "अगला कदम", select_pay_mode: "भुगतान का तरीका", proceed_pay: "भुगतान करें", manual_pay: "मैनुअल भुगतान", verify_transfer: "ट्रांसफर सत्यापित करें", earned: "कमाई", wins: "जीत", apply_coupon: "कूपन लगायें", match_history: "मैच का इतिहास", app_tutorial: "ऐप ट्यूटोरियल", refer_earn: "रेफर और कमाएं", settings: "सेटिंग्स", help_support: "सहायता", rules_policies: "नियम और नीतियां", logout: "लॉगआउट", no_tutorials: "कोई ट्यूटोरियल उपलब्ध नहीं।", language: "भाषा", select_theme: "प्रीमियम थीम चुनें", use_admin_theme: "एडमिन थीम लागू करें", hall_fame: "हॉल ऑफ फेम", match_earn: "मैच की कमाई", refer_reward: "रेफरल इनाम", loading: "लोड हो रहा है...", select_mode: "मोड चुनें" }
        };

        function changeLanguage(lang) {
            localStorage.setItem("app_lang", lang);
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if(translations[lang] && translations[lang][key]) el.textContent = translations[lang][key];
            });
            document.querySelectorAll('.lang-toggle-btn').forEach(btn => {
                btn.classList.toggle('active', btn.dataset.lang === lang);
                btn.style.borderColor = btn.dataset.lang === lang ? 'var(--accent-cyan)' : 'var(--border-glass)';
            });
        }

        function showToast(msg, type = "success") {
            const toast = document.getElementById('globalToast');
            if(!toast) return;
            toast.innerHTML = type === 'success' ? `<i class="bi bi-check-circle-fill me-2"></i> ${msg}` : `<i class="bi bi-exclamation-circle-fill me-2"></i> ${msg}`;
            toast.className = `custom-toast show ${type === 'error' ? 'toast-error' : 'toast-success'}`;
            setTimeout(() => toast.classList.remove('show'), 3000);
        }

        // ================= ADMIN & USER THEME LOGIC =================
        function applyCustomColors(colors) {
            const body = document.body;
            if(colors.bgColor) body.style.setProperty('--bg-base', colors.bgColor);
            if(colors.cardColor) body.style.setProperty('--bg-card', colors.cardColor);
            if(colors.headerColor) body.style.setProperty('--bg-surface', colors.headerColor);
            if(colors.btnColor) body.style.setProperty('--btn-custom-bg', colors.btnColor);
            if(colors.primaryColor) body.style.setProperty('--accent-cyan', colors.primaryColor);
            if(colors.secondaryColor) body.style.setProperty('--accent-purple', colors.secondaryColor);
            if(colors.textColor) body.style.setProperty('--text-main', colors.textColor);
            if(colors.headingColor) body.style.setProperty('--text-heading', colors.headingColor);
            if(colors.smallTextColor) body.style.setProperty('--text-muted', colors.smallTextColor);
            if(colors.borderColor) body.style.setProperty('--border-glass', colors.borderColor);
            
            if(colors.primaryColor && colors.secondaryColor) {
                body.style.setProperty('--gradient-primary', `linear-gradient(135deg, ${colors.primaryColor}, ${colors.secondaryColor})`);
                body.style.setProperty('--glow-shadow', `0 0 15px ${colors.primaryColor}55`);
            }
        }

        function resetCustomColors() {
            const body = document.body;
            ['--bg-base','--bg-card','--bg-surface','--btn-custom-bg','--accent-cyan','--accent-purple','--text-main','--text-heading','--text-muted','--border-glass','--gradient-primary','--glow-shadow'].forEach(v => body.style.removeProperty(v));
        }

        function applyTheme(themeName, isUserAction = false) {
            if (isUserAction && globalThemeLock) {
                return showToast("Admin has locked the theme.", "error");
            }
            document.body.className = themeName;
            if (isUserAction) localStorage.setItem("user_override_theme", themeName);
            localStorage.setItem("app_theme", themeName);
            document.querySelectorAll('.theme-card-select').forEach(card => card.classList.toggle('active', card.dataset.theme === themeName));
            document.querySelectorAll('.theme-mode-btn').forEach(btn => {
                btn.classList.toggle('active', btn.dataset.theme === themeName);
                btn.style.borderColor = btn.dataset.theme === themeName ? 'var(--accent-cyan)' : 'var(--border-glass)';
            });
        }

        function listenToThemeSettings() {
            onValue(ref(db, 'themeSettings'), (snap) => {
                if (snap.exists()) {
                    const data = snap.val();
                    globalThemeLock = data.themeLock === true;
                    currentAdminTheme = data.currentTheme || 'theme-neon';
                    const themeContainer = document.getElementById('themeSelectionContainer');
                    if (themeContainer) themeContainer.style.display = globalThemeLock ? 'none' : 'block';
                    const userOverride = localStorage.getItem("user_override_theme");
                    if (globalThemeLock) applyTheme(currentAdminTheme, false);
                    else if (userOverride) applyTheme(userOverride, false);
                    else applyTheme(currentAdminTheme, false);
                    if (data.customColors) applyCustomColors(data.customColors);
                    else resetCustomColors();
                } else {
                    globalThemeLock = false;
                    currentAdminTheme = 'theme-neon';
                    resetCustomColors();
                    const userOverride = localStorage.getItem("user_override_theme");
                    applyTheme(userOverride || currentAdminTheme, false);
                    const themeContainer = document.getElementById('themeSelectionContainer');
                    if (themeContainer) themeContainer.style.display = 'block';
                }
            });
        }

        // ================= ANNOUNCEMENT RUNNING TEXT SLIDER =================
        function listenToAnnouncements() {
            onValue(ref(db, 'announcements'), snap => {
                const container = document.getElementById('announcementBarContainer');
                const textEl = document.getElementById('announcementMarqueeText');
                if (!container || !textEl) return;
                if (snap.exists()) {
                    let activeAnns = []; let totalSpeed = 0;
                    snap.forEach(child => {
                        const data = child.val();
                        if (data.status === 'active' && data.text) { activeAnns.push(data.text); totalSpeed += (data.speed || 15); }
                    });
                    if (activeAnns.length > 0) {
                        textEl.innerHTML = activeAnns.join(' &nbsp;&nbsp;•&nbsp;&nbsp; ');
                        textEl.style.animationDuration = `${totalSpeed}s`;
                        container.style.display = 'block';
                    } else container.style.display = 'none';
                } else container.style.display = 'none';
            });
        }

        // ================= PROMOTION AUTO SLIDER =================
        window.promoTimeout = null;
        function listenToPromos() {
            onValue(ref(db, 'promotions'), snap => {
                const promos = [];
                if(snap.exists()) { snap.forEach(c => { const p = c.val(); if(p.active !== false) promos.push({...p, id: c.key}); }); }
                const cont = document.getElementById('promoSliderContainer');
                const track = document.getElementById('promoSliderTrack');
                if(!cont || !track) return;
                if(promos.length === 0) return cont.style.display = 'none';
                
                cont.style.display = 'block'; track.innerHTML = '';
                promos.forEach(p => {
                    const slide = document.createElement('div');
                    slide.style.minWidth = '100%'; slide.style.height = '100%';
                    slide.style.backgroundImage = `url('${p.imageUrl || 'https://via.placeholder.com/600x300'}')`;
                    slide.style.backgroundSize = 'cover'; slide.style.backgroundPosition = 'center'; slide.style.position = 'relative';
                    if(p.link) { slide.style.cursor = 'pointer'; slide.onclick = () => window.open(p.link, '_blank'); }
                    slide.innerHTML = `<div style="position:absolute; bottom:0; left:0; right:0; background:linear-gradient(transparent, rgba(0,0,0,0.9)); padding:15px;"><h6 class="text-white m-0 fw-bold" style="font-size:1rem;">${p.title || ''}</h6><small style="color:rgba(255,255,255,0.8); font-size:0.75rem;">${p.description || ''}</small></div>`;
                    track.appendChild(slide);
                });
                
                if(window.promoTimeout) clearTimeout(window.promoTimeout);
                let idx = 0;
                function nextSlide() {
                    const trackEl = document.getElementById('promoSliderTrack');
                    if(!trackEl) return;
                    idx = (idx + 1) % promos.length;
                    trackEl.style.transform = `translateX(-${idx * 100}%)`;
                    window.promoTimeout = setTimeout(nextSlide, (promos[idx].sliderTime || 5) * 1000);
                }
                if(promos.length > 1) window.promoTimeout = setTimeout(nextSlide, (promos[0].sliderTime || 5) * 1000);
            });
        }

        document.addEventListener('DOMContentLoaded', () => {
            modals = {
                withdraw: new bootstrap.Modal(document.getElementById('withdrawModalEl')),
                editName: new bootstrap.Modal(document.getElementById('editNameModal')),
                matchHistory: new bootstrap.Modal(document.getElementById('matchHistoryModal')),
                join: new bootstrap.Modal(document.getElementById('joinTournamentDetailsModal')),
                idPass: new bootstrap.Modal(document.getElementById('idPasswordModalEl')),
                matchDetails: new bootstrap.Modal(document.getElementById('matchDetailsModalEl')),
                orderStatus: new bootstrap.Modal(document.getElementById('orderStatusModalEl')),
                prizeList: new bootstrap.Modal(document.getElementById('prizeListModalEl'))
            };
            
            changeLanguage(localStorage.getItem("app_lang") || "en");
            
            document.querySelectorAll('.theme-card-select').forEach(card => card.addEventListener('click', () => applyTheme(card.dataset.theme, true)));
            document.querySelectorAll('.theme-mode-btn').forEach(btn => btn.addEventListener('click', () => applyTheme(btn.dataset.theme, true)));
            document.querySelectorAll('.lang-toggle-btn').forEach(btn => btn.addEventListener('click', () => changeLanguage(btn.dataset.lang)));

            const useAdminThemeBtn = document.getElementById('useAdminThemeBtn');
            if (useAdminThemeBtn) {
                useAdminThemeBtn.addEventListener('click', () => {
                    localStorage.removeItem("user_override_theme");
                    applyTheme(currentAdminTheme, false);
                    showToast("Reset to Admin Theme successfully!", "success");
                });
            }

            // My Contests 3-card click handlers (Ongoing / Upcoming / Results)
            document.querySelectorAll('#myContestsQuickGrid .contest-status-card').forEach(card => {
                const openStatus = () => {
                    const status = card.dataset.contestStatus || 'ongoing';
                    openMyContestsWithStatus(status);
                };
                card.addEventListener('click', openStatus);
                card.addEventListener('keydown', (e) => {
                    if (e.key === 'Enter' || e.key === ' ') {
                        e.preventDefault();
                        openStatus();
                    }
                });
            });

            // My Contests section tabs
            document.querySelectorAll('#myContestsTabsEl .tab-item').forEach(tab => {
                tab.addEventListener('click', (e) => {
                    const status = e.currentTarget.dataset.status || 'ongoing';
                    setActiveMyContestsTab(status);
                    loadMyContests(status);
                });
            });

            getEl('notificationBtnEl').onclick = (e) => { e.preventDefault(); e.stopPropagation(); document.getElementById("notificationOverlay").classList.add("show"); if (window.renderNotificationsList) window.renderNotificationsList(); };
            getEl('closeNotification').onclick = (e) => { e.preventDefault(); document.getElementById("notificationOverlay").classList.remove("show"); };

            if (typeof ZapUPI !== 'undefined' && typeof ZapUPI.setPaymentCallbacks === 'function') {
                ZapUPI.setPaymentCallbacks({
                    onSuccess: function(orderId) { verifyAndCreditZapUPI(orderId); },
                    onFailed: function(orderId) { showToast("Payment Failed. Order: " + orderId, "error"); showSection('wallet-section'); },
                    onTimeout: function(orderId) { showToast("Payment Timed Out. Order: " + orderId, "error"); showSection('wallet-section'); }
                });
            }

            listenToAppSettings();
            listenToThemeSettings();
            listenToAnnouncements();
            listenToPromos();
            listenToGamesAndModes();
        });

        function setActiveMyContestsTab(status) {
            currentMyContestStatus = status;
            document.querySelectorAll('#myContestsTabsEl .tab-item').forEach(tab => {
                tab.classList.toggle('active', tab.dataset.status === status);
            });
        }

        function openMyContestsWithStatus(status) {
            setActiveMyContestsTab(status);
            showSection('my-contests-section', 'home-section');
        }

        async function verifyAndCreditZapUPI(orderId) {
            if (typeof ZapUPI === 'undefined') return showToast("Payment SDK unavailable", "error");
            showLoader(true);
            try {
                const zapKey = appSettings?.payment?.zap_key;
                if(!zapKey) throw new Error("Gateway missing");
                ZapUPI.orderStatus({ zap_key: zapKey, order_id: orderId }, {
                    onResponse: async function(reqOrderId, data) {
                        try {
                            const d = data.data;
                            if(d && d.status === 'Success') {
                                const orderRef = ref(db, `orders/${orderId}`);
                                const orderSnap = await get(orderRef);
                                if (orderSnap.exists() && orderSnap.val().status === 'completed') {
                                    showToast("Payment already processed!", "success");
                                    return showLoader(false);
                                }
                                await runTransaction(ref(db, `users/${currentUser.uid}`), (user) => { if(user) user.balance = (Number(user.balance) || 0) + Number(d.amount); return user; });
                                await push(ref(db, 'deposits'), { userId: currentUser.uid, amount: Number(d.amount), utr: d.utr || d.txn_id || '-', paymentMethod: 'ZapUPI Auto', status: 'completed', timestamp: serverTimestamp() });
                                await update(orderRef, { status: 'completed', utr: d.utr || '', txnId: d.txn_id || '', completedAt: serverTimestamp() });
                                showToast('Payment Successful!', 'success'); showSection('wallet-section');
                            } else showToast("Payment status: " + (d?.status || "Unknown"), "error");
                        } catch(e) { showToast("Server update failed.", "error"); }
                        showLoader(false);
                    },
                    onError: function() { showLoader(false); showToast("Verification Failed.", "error"); }
                });
            } catch(e) { showLoader(false); showToast(e.message, "error"); }
        }

        const showLoader = (show) => { const el = document.getElementById('globalLoaderEl'); if(el) el.style.display = show ? 'flex' : 'none'; };
        const formatDate = (ts) => ts ? new Date(ts).toLocaleString('en-IN', { day: 'numeric', month: 'short', hour:'numeric', minute:'2-digit', hour12:true }) : 'N/A';
        function getTimeRemaining(startTime) { const diff = startTime - Date.now(); if (diff <= 0) return 'Live Now'; const d = Math.floor(diff/86400000), h = Math.floor((diff%86400000)/3600000), m = Math.floor((diff%3600000)/60000); return `${d>0?d+'d ':''}${h>0||d>0?h+'h ':''}${m}m`; }

        function fallbackCopyTextToClipboard(text, customMsg) {
            const successMsg = customMsg || 'Copied Successfully!';
            try { navigator.clipboard.writeText(text).then(() => showToast(successMsg, 'success')); } 
            catch(err) {
                let ta = document.createElement("textarea"); ta.value = text; ta.style.position = "fixed"; document.body.appendChild(ta); ta.focus(); ta.select();
                try { document.execCommand('copy'); showToast(successMsg, 'success'); } catch(e) { showToast('Failed to copy', 'error'); }
                document.body.removeChild(ta);
            }
        }

        function showSection(sectionId, backSection = null) {
            if (!auth) return;
            const target = document.getElementById(sectionId);
            if (!target) return showSection(currentUser ? 'home-section' : 'login-section');
            
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
            target.classList.add('active');
            currentSectionId = sectionId;

            const appHeader = document.querySelector('.app-header');
            const bottomNav = document.querySelector('.bottom-nav');
            if (sectionId === 'login-section') {
                if(appHeader) appHeader.style.display = 'none';
                if(bottomNav) bottomNav.style.display = 'none';
            } else {
                if(appHeader) appHeader.style.display = 'flex';
                if(bottomNav) bottomNav.style.display = 'flex';
            }
            
            document.querySelectorAll('.bottom-nav .nav-item').forEach(item => item.classList.toggle('active', item.dataset.section === sectionId));
            
            const showBack = ['tournaments-section', 'modes-section', 'my-contests-section', 'recharge-section', 'support-section', 'referral-section', 'policies-section', 'settings-section', 'tutorials-section'].includes(sectionId);
            getEl('headerTitleContainerEl').style.display = !showBack ? 'flex' : 'none';
            getEl('headerBackBtnEl').style.display = showBack ? 'inline-block' : 'none';
            
            if(showBack) {
                getEl('headerBackBtnEl').onclick = () => {
                    if (sectionId === 'tournaments-section' && currentTournamentModeId) showSection('modes-section', 'home-section');
                    else showSection(backSection || 'home-section');
                };
            }
            
            getEl('headerGameTitleEl').style.display = showBack ? 'block' : 'none';
            
            const activeLang = localStorage.getItem("app_lang") || "en";
            if (sectionId === 'modes-section' && currentTournamentGameId) {
                const gName = allGames[currentTournamentGameId]?.name || 'GAME MODES';
                getEl('headerGameTitleEl').innerHTML = `<span style="font-size:1.1rem; font-weight:800; letter-spacing:1px; text-transform:uppercase;" class="text-gradient">${gName}</span>`;
            }
            else if (sectionId === 'tournaments-section' && currentTournamentGameId) {
                const gName = allGames[currentTournamentGameId]?.name || 'Game';
                const mName = currentTournamentModeId && allModes[currentTournamentModeId]?.name ? allModes[currentTournamentModeId].name : 'Matches';
                getEl('headerGameTitleEl').innerHTML = `<span style="font-size:0.65rem; color:var(--accent-cyan); display:block; line-height:1;">${gName}</span><span style="font-size:1rem; line-height:1.2; color:var(--text-main); font-weight:700;">${mName}</span>`;
            }
            else if (sectionId === 'my-contests-section') getEl('headerGameTitleEl').innerHTML = `<span class="text-main fw-bold">${translations[activeLang]?.my_contests || 'My Contests'}</span>`;
            else if (sectionId === 'recharge-section') getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Add Funds</span>';
            else if (sectionId === 'support-section') getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Support</span>';
            else if (sectionId === 'referral-section') getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Refer & Earn</span>';
            else if (sectionId === 'policies-section') getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Rules & Policies</span>';
            else if (sectionId === 'settings-section') getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Settings</span>';
            else if (sectionId === 'tutorials-section') { getEl('headerGameTitleEl').innerHTML = '<span class="text-main fw-bold">Tutorials</span>'; loadTutorials(); }

            if(sectionId === 'home-section') { loadGames(); }
            if(sectionId === 'my-contests-section') { loadMyContests(currentMyContestStatus); }
            if(sectionId === 'leaderboard-section') loadLeaderboard();
            if(sectionId === 'modes-section' && currentTournamentGameId) loadModes(currentTournamentGameId);
            if(sectionId === 'tournaments-section' && currentTournamentGameId) {
                const activeTab = document.querySelector('#tournamentsTabsEl .active');
                filterTournaments(currentTournamentGameId, currentTournamentModeId, activeTab ? activeTab.dataset.status : 'upcoming');
            }
            if(sectionId === 'wallet-section') renderWalletHistory();
            if(sectionId === 'profile-section') fetchUserMatchStats();
            window.scrollTo(0, 0);
        }

        document.addEventListener('click', (e) => {
            const btn = e.target.closest('[data-section]');
            if(btn) {
                e.preventDefault();
                const target = btn.dataset.section;
                if(target === 'matchhistory-trigger') { modals.matchHistory.show(); loadMatchHistory(); }
                else showSection(target, (target.includes('policies') || target.includes('referral') || target.includes('support') || target.includes('settings') || target.includes('tutorials')) ? 'profile-section' : 'home-section');
            }

            const copyBtn = e.target.closest('.copy-btn');
            if(copyBtn) {
                e.preventDefault();
                if(copyBtn.classList.contains('disabled')) return showToast("Action disabled", "error");
                let text = copyBtn.dataset.text || document.querySelector(copyBtn.dataset.target)?.textContent.trim();
                if(text && !text.includes("Generating") && !text.includes("Disabled") && text !== "----" && text !== "DISABLED") {
                    let msg = copyBtn.dataset.target === '#myReferralLinkEl' ? 'Referral Link Copied Successfully' : 'Copied Successfully!';
                    fallbackCopyTextToClipboard(text, msg);
                    const icon = copyBtn.querySelector('i');
                    if (icon) {
                        const originalClass = icon.className;
                        icon.className = 'bi bi-check2-circle';
                        setTimeout(() => icon.className = originalClass, 1500);
                    }
                } else { showToast('Invalid content to copy', 'error'); }
            }
        });

        // ================= CORE AUTH =================
        async function generateReferralCode() {
            const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'; let code = '';
            for(let i=0; i<(Math.random()>0.5?3:4); i++) code += chars.charAt(Math.floor(Math.random() * chars.length));
            try {
                const snap = await get(query(ref(db, 'users'), orderByChild('referralCode'), equalTo(code)));
                if(snap.exists()) return await generateReferralCode(); 
                return code;
            } catch(e) { return code; } 
        }

        onAuthStateChanged(auth, async (user) => {
            showLoader(true); 
            clearUserListeners();
            currentUser = user;
            if (user) {
                getEl('notificationBtnEl').style.display = 'flex';
                const uRef = ref(db, 'users/' + user.uid);
                
                const uCallback = onValue(uRef, async (s) => { 
                    if(s.exists()){ 
                        userProfile = s.val(); 
                        if(!userProfile.referralCode) {
                            const newRefCode = await generateReferralCode();
                            await update(uRef, { referralCode: newRefCode });
                            userProfile.referralCode = newRefCode;
                        }
                        updateUIForUser(); 
                        setupReferralSystem();
                        if(currentSectionId === 'my-contests-section') loadMyContests(currentMyContestStatus);
                    } else {
                        const refCode = await generateReferralCode();
                        userProfile = { uid: user.uid, displayName: user.email?.split('@')[0], email: user.email, balance: appSettings.signupBonus ?? 10, winningCash: 0, bonusCash: appSettings.signupBonus ?? 10, joinedTournaments: {}, referralCode: refCode, createdAt: serverTimestamp() };
                        await set(uRef, userProfile);
                        updateUIForUser();
                        setupReferralSystem();
                    }
                });
                activeUserListener = { ref: uRef, callback: uCallback };
                
                if (!activeTournamentsListener) {
                    const tRef = ref(db, 'tournaments');
                    const tCallback = onValue(tRef, (snap) => {
                        allTournamentsData = snap.val() || {};
                        if(currentSectionId === 'my-contests-section') loadMyContests(currentMyContestStatus);
                        if(currentSectionId === 'tournaments-section' && currentTournamentGameId) {
                            const activeTab = document.querySelector('#tournamentsTabsEl .active');
                            filterTournaments(currentTournamentGameId, currentTournamentModeId, activeTab ? activeTab.dataset.status : 'upcoming');
                        }
                        listenToWalletHistory();
                        fetchUserMatchStats();
                    });
                    activeTournamentsListener = { ref: tRef, callback: tCallback };
                }
                
                listenToWalletHistory();
                listenToNotifications();
                showSection(currentSectionId !== 'login-section' ? currentSectionId : 'home-section');
            } else { 
                getEl('notificationBtnEl').style.display = 'none';
                getEl('headerWalletChipEl').style.display='none'; 
                showSection('login-section'); 
            }
            showLoader(false);
        });

        getEl('loginEmailBtnEl').onclick = async () => {
            showLoader(true);
            try { await signInWithEmailAndPassword(auth, getEl('loginEmailInputEl').value, getEl('loginPasswordInputEl').value); } 
            catch (e) { showToast("Login failed. Check details.", "error"); } finally { showLoader(false); }
        };

        getEl('signupEmailBtnEl').onclick = async () => {
            const name = getEl('signupNameInputEl').value, em = getEl('signupEmailInputEl').value, pw = getEl('signupPasswordInputEl').value;
            if(!name || pw.length<6) return showToast('Enter name and min 6 char password.', "error");
            showLoader(true);
            try { 
                const cred = await createUserWithEmailAndPassword(auth, em, pw); 
                const newRefCode = await generateReferralCode();
                await update(ref(db, `users/${cred.user.uid}`), { displayName: name, referralCode: newRefCode });
                
                const refCodeInput = getEl('signupReferralCodeInputEl').value.trim().toUpperCase();
                if(refCodeInput) {
                    const snap = await get(query(ref(db, 'users'), orderByChild('referralCode'), equalTo(refCodeInput)));
                    if(snap.exists()) {
                        const referrerUid = Object.keys(snap.val())[0];
                        await push(ref(db, 'pendingReferrals'), {referrerUid: referrerUid, referredEmail: em, status: 'pending', timestamp: serverTimestamp()});
                    }
                }
            } catch (e) { showToast(e.message, "error"); } finally { showLoader(false); }
        };

        getEl('showSignupToggleBtnEl').onclick = () => { getEl('emailLoginForm').style.display='none'; getEl('emailSignupForm').style.display='block'; };
        getEl('showLoginToggleBtnEl').onclick = () => { getEl('emailLoginForm').style.display='block'; getEl('emailSignupForm').style.display='none'; };
        getEl('logoutProfileBtnEl').onclick = () => signOut(auth);

        // ================= ASYNC STATS FETCH =================
        function fetchUserMatchStats() {
            if(!currentUser) return;
            let totalM = 0; let wonM = 0;
            Object.values(allTournamentsData).forEach(t => {
                if(t.registeredPlayers && t.registeredPlayers[currentUser.uid]) {
                    totalM++;
                    const pData = t.registeredPlayers[currentUser.uid];
                    if(Number(pData.prize) > 0 || Number(pData.rank) === 1 || pData.matchStatus === 'winner') wonM++;
                }
            });
            clearPlaceholders('profileStatsGridContainer', 'profileStatsGridContainer');
            const tmEl = getEl('profileTotalMatchesEl');
            if(tmEl) { tmEl.innerHTML = totalM; tmEl.classList.remove('placeholder', 'col-6'); }
            const wmEl = getEl('profileWonMatchesEl');
            if(wmEl) { wmEl.innerHTML = wonM; wmEl.classList.remove('placeholder', 'col-6'); }
            userProfile.totalMatches = totalM;
            userProfile.wonMatches = wonM;
        }

        // ================= UI PERMISSIONS & UPDATES =================
        function listenToAppSettings() {
            onValue(ref(db, 'settings'), (snap) => {
                if(snap.exists()) { appSettings = Object.assign(appSettings, snap.val()); } 
                else { appSettings = { minWithdraw: 50, signupBonus: 10, referralBonus: 10, referralEnabled: true, paymentGateway: 'manual', appName: 'MrBattleZone' }; }
                updateAppUIWithSettings();
                if(currentUser && userProfile) { updateUIForUser(); setupReferralSystem(); }
            });
        }

        function listenToGamesAndModes() {
            onValue(ref(db, 'games'), (snap) => { allGames = snap.val() || {}; if(currentSectionId === 'home-section') loadGames(); });
            onValue(ref(db, 'modes'), (snap) => { allModes = snap.val() || {}; if(currentSectionId === 'modes-section' && currentTournamentGameId) loadModes(currentTournamentGameId); });
        }

        function updateAppUIWithSettings() {
            document.querySelectorAll('.app-logo-img').forEach(img => img.src = appSettings.logoUrl || 'https://via.placeholder.com/100');
            document.querySelectorAll('.app-name-text').forEach(el => el.textContent = appSettings.appName || 'MrBattleZone');

            const minDep = appSettings.payment?.min_deposit || 10, maxDep = appSettings.payment?.max_deposit || 50000;
            if(getEl('rechargeAmountInput').tagName) { getEl('rechargeAmountInput').min = minDep; getEl('rechargeAmountInput').max = maxDep; }
            if(getEl('rechargeLimitLabelEl').tagName) getEl('rechargeLimitLabelEl').innerHTML = `Enter Amount (<span class="c-sym"></span>${minDep} - <span class="c-sym"></span>${maxDep})`;
            if(getEl('minWithdrawAmountEl').tagName) getEl('minWithdrawAmountEl').textContent = appSettings.minWithdraw || 50;
            if(getEl('minRedeemAmountEl').tagName) getEl('minRedeemAmountEl').textContent = appSettings.minWithdraw || 50;

            if(appSettings.payment?.gateway_enabled === true && getEl('optionAutoCard').tagName) getEl('optionAutoCard').style.display = 'flex';
            else if (getEl('optionAutoCard').tagName){ getEl('optionAutoCard').style.display = 'none'; getEl('optionManualCard')?.querySelector('input')?.setAttribute('checked','true'); }

            const waBtn = document.getElementById('supportWaBtn'), tgBtn = document.getElementById('supportTgBtn'), noMsg = document.getElementById('noSupportLinksMsg');
            if(waBtn) { waBtn.style.display = 'none'; tgBtn.style.display = 'none'; noMsg.style.display = 'none';
                let c = 0;
                if(appSettings.supportWa && appSettings.isWaActive !== false) { waBtn.href = appSettings.supportWa; waBtn.style.display = 'inline-flex'; c++; }
                if(appSettings.supportTg && appSettings.isTgActive !== false) { tgBtn.href = appSettings.supportTg; tgBtn.style.display = 'inline-flex'; c++; }
                if(c===0) noMsg.style.display = 'block';
            }

            const polDiv = document.getElementById('policiesAccordion');
            if(polDiv) {
                polDiv.className = "accordion premium-accordion";
                const pol = [ 
                    {id:'t', title:'Terms & Conditions', icon:'file-earmark-text', txt: appSettings.policyTerms||'Not available.'}, 
                    {id:'p', title:'Privacy Policy', icon:'shield-lock', txt: appSettings.policyPrivacy||'Not available.'}, 
                    {id:'r', title:'Refund & Cancellation', icon:'arrow-counterclockwise', txt: appSettings.policyRefund||'Not available.'},
                    {id:'f', title:'FairPlay Policy', icon:'controller', txt: appSettings.policyFairPlay||'Not available.'} 
                ];
                polDiv.innerHTML = pol.map(p => `
                <div class="accordion-item">
                    <h2 class="accordion-header">
                        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#c${p.id}">
                            <i class="bi bi-${p.icon} me-2" style="font-size: 1.2rem; color: var(--accent-purple);"></i> ${p.title}
                        </button>
                    </h2>
                    <div id="c${p.id}" class="accordion-collapse collapse" data-bs-parent="#policiesAccordion">
                        <div class="accordion-body">
                            ${p.txt.replace(/\n/g, '<br>')}
                        </div>
                    </div>
                </div>`).join('');
            }

            document.querySelectorAll('.list-group-item').forEach(item => {
                const sec = item.dataset.section;
                if (sec === 'referral-section') item.style.display = appSettings.referralEnabled === false ? 'none' : 'flex';
                if (sec === 'tutorials-section') item.style.display = appSettings.tutorialsEnabled === false ? 'none' : 'flex';
                if (sec === 'support-section') item.style.display = appSettings.supportEnabled === false ? 'none' : 'flex';
            });
            
            applyCurrencySymbol();
        }

        function updateUIForUser() {
            if (!userProfile) return;
            const dep = parseFloat(userProfile.balance) || 0;
            const win = parseFloat(userProfile.winningCash) || 0;
            const bon = parseFloat(userProfile.bonusCash) || 0;
            const usable = dep + win;
            const total = dep + win + bon;

            getEl('headerWalletChipEl').style.display='flex'; 
            
            document.querySelectorAll('.bottom-nav .nav-item').forEach(i => {
                const sec = i.dataset.section;
                if (sec === 'leaderboard-section' && appSettings.leaderboardEnabled === false) i.style.display = 'none';
                else if (sec === 'earnings-section' && appSettings.earningsEnabled === false) i.style.display = 'none';
                else if (sec === 'wallet-section' && appSettings.walletEnabled === false) i.style.display = 'none';
                else i.style.display = 'flex';
            });

            const safeName = safeStr(userProfile.displayName || userProfile.email?.split('@')[0], 'Player').trim();
            const safeEmail = safeStr(userProfile.email, 'No Email').trim();
            
            getEl('headerUserGreetingEl').textContent = `Hi, ${safeName.split(' ')[0]}`; 
            getEl('headerUserGreetingEl').style.display = 'block';
            getEl('headerChipBalanceEl').textContent = Math.floor(usable);
            
            getEl('profileAvatarEl').src = `https://ui-avatars.com/api/?name=${encodeURIComponent(safeName)}&background=18181b&color=06b6d4&bold=true`;
            clearPlaceholders('profileAvatarEl', 'profileAvatarContainer');
            getEl('editNameBtnEl').classList.remove('d-none');

            getEl('profileNameEl').innerHTML = safeName; 
            clearPlaceholders('profileNameEl');
            
            getEl('profileEmailEl').innerHTML = safeEmail;
            clearPlaceholders('profileEmailEl');
            
            getEl('profileRefCodeEl').innerHTML = `<i class="bi bi-gift-fill me-1"></i> My Code: <strong class="text-white">${userProfile.referralCode || 'N/A'}</strong>`;
            
            getEl('profileTotalMatchesEl').innerHTML = userProfile.totalMatches || Object.keys(userProfile.joinedTournaments||{}).length || 0; 
            clearPlaceholders('profileTotalMatchesEl');
            
            getEl('profileWonMatchesEl').innerHTML = userProfile.wonMatches || 0;
            clearPlaceholders('profileWonMatchesEl');
            
            getEl('profileTotalEarningsEl').innerHTML = window.FMT_C(win);
            clearPlaceholders('profileTotalEarningsEl');

            if(currentSectionId === 'profile-section') fetchUserMatchStats();
            
            getEl('earningsTotalEl').innerHTML = window.FMT_C(win); 
            clearPlaceholders('earningsTotalEl', 'earningsTotalContainer');
            
            getEl('earningsReferralEl').innerHTML = window.FMT_C(bon);
            clearPlaceholders('earningsReferralEl', 'earningsReferralContainer');

            getEl('walletTotalBalanceEl').innerHTML = window.FMT_C(total); 
            clearPlaceholders('walletTotalBalanceEl', 'walletTotalBalanceContainer');
            
            getEl('walletWinningCashEl').innerHTML = window.FMT_C(win); 
            clearPlaceholders('walletWinningCashEl', 'walletSplitContainer');
            
            getEl('walletBonusCashEl').innerHTML = window.FMT_C(bon);
            clearPlaceholders('walletBonusCashEl');

            getEl('withdrawModalBalanceEl').innerHTML = window.FMT_C(win);
        }

        function setupReferralSystem() {
            if (!currentUser || !userProfile) return;
            const refLinkEl = document.getElementById('myReferralLinkEl');
            const bonusTextEl = document.getElementById('referralBonusText');
            const copyBtns = document.querySelectorAll('#referral-section .copy-btn');

            if (appSettings.referralEnabled === false) {
                if(refLinkEl) refLinkEl.textContent = "Referral System Disabled";
                if(bonusTextEl) bonusTextEl.textContent = window.FMT_C(0);
                copyBtns.forEach(btn => btn.classList.add('disabled', 'opacity-50'));
                return;
            }

            copyBtns.forEach(btn => btn.classList.remove('disabled', 'opacity-50'));
            if(bonusTextEl) bonusTextEl.innerHTML = window.FMT_C(appSettings.referralBonus || 0);
            
            if (userProfile.referralCode && refLinkEl) {
                let linkBase = appSettings.demoLink || window.location.origin;
                linkBase = linkBase.replace(/\/$/, ""); 
                refLinkEl.textContent = `${linkBase}/?ref=${userProfile.referralCode}`;
            } else if (refLinkEl) refLinkEl.textContent = "Generating...";

            loadReferralStats();
        }

        async function loadReferralStats() {
            if(!currentUser) return;
            if(activeReferralsListener) return;

            const refQ = query(ref(db, 'pendingReferrals'), orderByChild('referrerUid'), equalTo(currentUser.uid));
            activeReferralsListener = {
                ref: refQ,
                callback: onValue(refQ, (snap) => {
                    let totalInvited = 0, totalEarned = 0;
                    if(snap.exists()) {
                        snap.forEach(child => {
                            totalInvited++;
                            const data = child.val();
                            if(data.status === 'completed') totalEarned += (Number(data.bonusAmount) || 0);
                        });
                    }
                    const invEl = document.getElementById('referralTotalJoinedEl');
                    const earnEl = document.getElementById('referralTotalEarnedEl');
                    if (invEl) invEl.textContent = totalInvited;
                    if (earnEl) earnEl.innerHTML = window.FMT_C(totalEarned);
                })
            };
        }

        // ================= WALLET HISTORY =================
        function renderWalletHistory() {
            const list = document.getElementById('walletHistoryListEl'); 
            if(!list) return;
            list.classList.remove('placeholder-glow');
            userTxns.sort((a,b) => b.time - a.time);
            list.innerHTML = '';
            if(userTxns.length === 0) { list.innerHTML = '<div class="text-center py-4 text-muted fw-bold">No transactions yet.</div>'; return; }
            
            userTxns.forEach(t => {
                const isD = ['Deposit', 'Refund', 'Gift Code', 'Manual Deposit', 'Winnings', 'Referral Bonus'].includes(t.type);
                const isRedeem = t.type === 'Redeem Code';
                let icon = 'bi-arrow-up-right-circle-fill';
                if(isD) icon = 'bi-arrow-down-left-circle-fill';
                if(t.type.includes('Code')) icon = 'bi-gift-fill';
                if(t.type === 'Winnings') icon = 'bi-trophy-fill';
                if(t.type === 'Referral Bonus') icon = 'bi-people-fill';
                
                const st = (t.status==='completed'||t.status==='success'||t.status==='Success') ? 'Success' : (t.status==='pending' ? 'Pending' : 'Failed');
                let col = '#ef4444'; 
                if (st === 'Success') col = '#10b981'; 
                else if (st === 'Pending') col = '#f59e0b'; 
                
                let extraUI = '';
                if (isRedeem) {
                    if (st === 'Success') {
                        const code = t.adminNote || 'Check Support';
                        extraUI = `<div class="mt-3 p-2 rounded d-flex justify-content-between align-items-center" style="background: rgba(16, 185, 129, 0.1); border: 1px dashed #10b981;"><strong style="color: #10b981; font-family: monospace; font-size: 1.05rem; letter-spacing: 2px;">${code}</strong><button class="btn btn-sm py-1 px-2 copy-btn text-white" style="background: #10b981; border-radius: 6px;" data-text="${code}"><i class="bi bi-clipboard"></i></button></div>`;
                    } else if (st === 'Failed') extraUI = `<div class="mt-2 p-2 rounded text-danger small fw-bold" style="background: rgba(239, 68, 68, 0.1);"><i class="bi bi-x-circle-fill"></i> Reason: ${t.rejectReason || 'Declined by Admin'}</div>`;
                    else extraUI = `<div class="mt-2 p-2 rounded text-warning small fw-bold" style="background: rgba(245, 158, 11, 0.1);"><i class="bi bi-hourglass-split"></i> Awaiting Admin Approval</div>`;
                } else {
                    if (st === 'Failed') extraUI = `<div class="mt-2 p-2 rounded text-danger small fw-bold" style="background: rgba(239, 68, 68, 0.1);"><i class="bi bi-x-circle-fill"></i> Reason: ${t.rejectReason || 'Declined'}</div>`;
                    else if (st === 'Success' && t.adminNote) extraUI = `<div class="mt-2 p-2 rounded text-success small fw-bold" style="background: rgba(16, 185, 129, 0.1);"><i class="bi bi-info-circle-fill"></i> Ref: ${t.adminNote}</div>`;
                }

                const methodStr = t.paymentMethod || t.methodDetails?.accountInfo || t.method || (isRedeem ? 'Play Store Code' : (t.type === 'Winnings' ? 'Match Prize' : 'Bank/UPI'));

                list.innerHTML += `<div class="glass-card p-3 mb-3" style="border-left: 4px solid ${col}; border-color: var(--border-glass) var(--border-glass) var(--border-glass) ${col} !important;">
                    <div class="d-flex justify-content-between align-items-center">
                        <div class="d-flex align-items-center gap-3">
                            <i class="bi ${icon} fs-3" style="color:${col}; filter: drop-shadow(0 0 5px ${col});"></i>
                            <div>
                                <h6 class="fw-bold mb-0 text-main">${t.type} <span class="badge ms-1" style="font-size:0.6rem; background: ${col}22; color:${col}; border: 1px solid ${col}55;">${st}</span></h6>
                                <span style="font-size:0.7rem; color:var(--text-muted);">${formatDate(t.time)}</span>
                            </div>
                        </div>
                        <div class="text-end">
                            <h5 class="m-0 fw-bold glow-text d-flex justify-content-end align-items-center" style="color:${col};">${isD?'+':'-'}${window.FMT_C(t.amount)}</h5>
                            <small class="text-muted text-truncate d-inline-block" style="font-size: 0.65rem; max-width: 100px;">${methodStr}</small>
                        </div>
                    </div>
                    ${extraUI}
                </div>`;
            });
        }

        function listenToWalletHistory() {
            if(!currentUser) return;
            const list = document.getElementById('walletHistoryListEl'); 
            if(list && userTxns.length === 0) list.innerHTML = '<div class="text-center py-4"><div class="spinner-border glow-text" style="color:var(--accent-cyan);"></div></div>';

            const depRef = query(ref(db, 'deposits'), orderByChild('userId'), equalTo(currentUser.uid));
            const withRef = query(ref(db, 'withdrawals'), orderByChild('userId'), equalTo(currentUser.uid));
            const refRef = query(ref(db, 'pendingReferrals'), orderByChild('referrerUid'), equalTo(currentUser.uid));

            let deposits = [], withdrawals = [], referralsList = [];

            const updateTxns = () => {
                userTxns = [];
                deposits.forEach(d => {
                    let type = 'Deposit';
                    if (d.paymentMethod?.includes('REFUND') || d.paymentMethod?.includes('REFUND:')) type = 'Refund';
                    else if (d.paymentMethod?.includes('Redeem Code')) type = 'Gift Code';
                    else if (d.paymentMethod?.includes('Manual')) type = 'Manual Deposit';
                    userTxns.push({...d, type, time: d.timestamp || d.processedAt || 0});
                });
                withdrawals.forEach(w => { userTxns.push({...w, type: w.withdrawalType === 'redeem' ? 'Redeem Code' : 'Withdraw', time: w.requestTimestamp || w.processedAt || 0}); });
                Object.values(allTournamentsData).forEach(t => {
                    if (t.winningsCredited && t.registeredPlayers?.[currentUser.uid]) {
                        const pData = t.registeredPlayers[currentUser.uid];
                        const pz = Number(pData.prize || 0) + Number(pData.extraPrize || 0) + Number(pData.bonus || 0);
                        if(pz > 0) userTxns.push({ id: t.id+'_win', type: 'Winnings', amount: pz, status: 'Success', time: t.endTime || t.startTime || 0, adminNote: t.name });
                    }
                });
                referralsList.forEach(r => { if(r.status === 'completed') userTxns.push({ id: r.id, type: 'Referral Bonus', amount: r.bonusAmount, status: 'Success', time: r.creditedAt }); });
                if(currentSectionId === 'wallet-section') renderWalletHistory();
            };

            if(!activeDepositsListener) activeDepositsListener = { ref: depRef, callback: onValue(depRef, snap => { deposits = []; if(snap.exists()) snap.forEach(c => deposits.push({...c.val(), id: c.key})); updateTxns(); }) };
            if(!activeWithdrawalsListener) activeWithdrawalsListener = { ref: withRef, callback: onValue(withRef, snap => { withdrawals = []; if(snap.exists()) snap.forEach(c => withdrawals.push({...c.val(), id: c.key})); updateTxns(); }) };
            onValue(refRef, snap => { referralsList = []; if(snap.exists()) snap.forEach(c => referralsList.push({...c.val(), id: c.key})); updateTxns(); });
            updateTxns();
        }

        // ================= PROMO / REDEEM =================
        document.getElementById('applyRedeemBtnEl')?.addEventListener('click', async () => {
            const code = getEl('redeemCodeInput').value.trim().toUpperCase();
            if(!code) return showToast("Enter code", "error");
            showLoader(true);
            try {
                const res = await runTransaction(ref(db, `redeemCodes/${code}`), (data) => {
                    if (data === null) return data;
                    if (data.status === 'active' && !data.usedBy) { data.status = 'used'; data.usedBy = currentUser.uid; data.usedAt = Date.now(); return data; }
                    return; 
                });
                if(res.committed && res.snapshot.exists()) {
                    const amount = Number(res.snapshot.val().amount || 0);
                    await runTransaction(ref(db, `users/${currentUser.uid}`), user => { if(user) user.balance = (Number(user.balance)||0) + amount; return user; });
                    await push(ref(db, 'deposits'), { userId: currentUser.uid, amount: amount, paymentMethod: 'Redeem Code', status: 'completed', timestamp: serverTimestamp() });
                    showToast(`Success! ${window.FMT_C(amount)} added`, "success"); getEl('redeemCodeInput').value = '';
                } else showToast("Invalid or used code", "error");
            } catch(e) { showToast("Error applying code", "error"); }
            showLoader(false);
        });

        document.getElementById('applyCouponBtnEl')?.addEventListener('click', async () => {
            const code = getEl('couponCodeInput').value.trim().toUpperCase();
            if(!code) return showToast("Enter code", "error");
            showLoader(true);
            try {
                const res = await runTransaction(ref(db, `couponCodes/${code}`), (data) => {
                    if (data === null) return data;
                    if (data.status === 'active') {
                        if (!data.usedUsers) data.usedUsers = {};
                        if (!data.usedUsers[currentUser.uid]) { data.usedUsers[currentUser.uid] = true; return data; }
                    }
                    return; 
                });
                if(res.committed && res.snapshot.exists()) {
                    const amount = Number(res.snapshot.val().amount || 0);
                    await runTransaction(ref(db, `users/${currentUser.uid}`), user => { if(user) user.bonusCash = (Number(user.bonusCash)||0) + amount; return user; });
                    showToast(`Coupon applied! ${window.FMT_C(amount)} Bonus added`, "success"); getEl('couponCodeInput').value = '';
                } else showToast("Invalid or already used", "error");
            } catch(e) { showToast("Error applying coupon", "error"); }
            showLoader(false);
        });

        async function loadTutorials() {
            const container = document.getElementById('tutorialsListEl');
            container.classList.remove('placeholder-glow');
            container.innerHTML = '<div class="text-center"><div class="spinner-border text-primary"></div></div>'; getEl('noTutorialsMsg').style.display='none';
            try {
                const snap = await get(ref(db, 'tutorials'));
                if(!snap.exists()) { container.innerHTML=''; getEl('noTutorialsMsg').style.display='block'; return; }
                container.innerHTML = '';
                Object.values(snap.val()).forEach(t => { container.innerHTML += `<div class="glass-card mb-3 p-0 overflow-hidden"><div class="position-relative" style="padding-bottom:56.25%;"><iframe style="position:absolute; top:0; left:0; width:100%; height:100%; border:none;" src="${t.videoUrl}" allowfullscreen></iframe></div><div class="p-3"><h6 class="fw-bold m-0 text-main">${t.title || 'Tutorial'}</h6><p class="text-muted small mt-1 mb-0">${t.description || ''}</p></div></div>`; });
            } catch(e) { container.innerHTML = ''; getEl('noTutorialsMsg').style.display='block'; }
        }

        // ================= GAMES & MODES INTEGRATION =================
        function loadGames() {
            const list = document.getElementById('gamesListEl');
            if(!list) return;
            const games = Object.entries(allGames);
            list.classList.remove('placeholder-glow'); list.innerHTML = '';
            if(games.length > 0) { 
                games.forEach(([id, g]) => { if(g.status === 'inactive') return; list.innerHTML += `<div class="game-card-new" style="background-image:url('${g.imageUrl || g.logo || 'https://via.placeholder.com/150'}')" data-id="${id}"><div class="game-card-new-overlay"><span>${g.name}</span></div></div>`; });
                list.querySelectorAll('.game-card-new').forEach(c => {
                    c.onclick = () => { 
                        currentTournamentGameId = c.dataset.id;
                        const hasModes = Object.values(allModes).some(m => m.gameId === currentTournamentGameId && m.status !== 'inactive');
                        if(hasModes) { loadModes(currentTournamentGameId); showSection('modes-section', 'home-section'); } 
                        else {
                            currentTournamentModeId = null;
                            showSection('tournaments-section', 'home-section');
                            const activeTab = document.querySelector('#tournamentsTabsEl .active');
                            filterTournaments(currentTournamentGameId, null, activeTab ? activeTab.dataset.status : 'upcoming');
                        }
                    };
                });
            }
        }

        function loadModes(gameId) {
            const gData = allGames[gameId]; if(!gData) return;
            const list = getEl('modesListEl'); list.innerHTML = '';
            const modesArray = Object.entries(allModes).filter(([, m]) => m.gameId === gameId && m.status !== 'inactive');
            modesArray.sort((a,b) => (a[1].sortOrder||0) - (b[1].sortOrder||0));
            modesArray.forEach(([mId, m]) => { list.innerHTML += `<div class="mode-card" style="background-image:url('${m.thumbnailUrl || m.logo || gData.imageUrl || gData.logo || 'https://via.placeholder.com/150'}')" data-id="${mId}" data-name="${m.modeName || m.name}"><div class="mode-card-overlay"><span>${m.modeName || m.name}</span></div></div>`; });
            list.querySelectorAll('.mode-card').forEach(c => {
                c.onclick = () => {
                    currentTournamentModeId = c.dataset.id;
                    showSection('tournaments-section', 'modes-section');
                    const activeTab = document.querySelector('#tournamentsTabsEl .active');
                    filterTournaments(currentTournamentGameId, currentTournamentModeId, activeTab ? activeTab.dataset.status : 'upcoming');
                };
            });
        }

        function loadMyContests(filterStatus = currentMyContestStatus) {
            const status = filterStatus || 'ongoing';
            const joined = Object.keys(userProfile?.joinedTournaments || {});
            const listEl = document.getElementById('myContestsListEl');
            const emptyEl = document.getElementById('noContestsMessageEl');
            const emptyTextEl = document.getElementById('noContestsTextEl');
            if(!listEl || !emptyEl) return;

            listEl.classList.remove('placeholder-glow');
            listEl.innerHTML = '';

            const lang = localStorage.getItem("app_lang") || "en";
            const emptyMsgKey = status === 'ongoing' ? 'no_ongoing_matches' : (status === 'upcoming' ? 'no_upcoming_matches' : 'no_completed_matches');
            if (emptyTextEl && translations[lang]?.[emptyMsgKey]) {
                emptyTextEl.textContent = translations[lang][emptyMsgKey];
            }

            if(joined.length === 0) {
                emptyEl.style.display = 'block';
                return;
            }

            const matched = [];
            for (const id of joined) {
                const t = allTournamentsData[id];
                if (!t) continue;
                const tStatus = t.status || 'upcoming';
                const isMatch = (status === 'completed')
                    ? (tStatus === 'completed' || tStatus === 'result' || tStatus === 'canceled')
                    : (tStatus === status);
                if (isMatch) matched.push([id, t]);
            }

            if (status === 'completed') {
                matched.sort(([, a], [, b]) => (b.startTime || 0) - (a.startTime || 0));
            } else {
                matched.sort(([, a], [, b]) => (a.startTime || 0) - (b.startTime || 0));
            }

            if (matched.length === 0) {
                emptyEl.style.display = 'block';
                return;
            }

            emptyEl.style.display = 'none';
            matched.forEach(([id, t]) => listEl.appendChild(createCard(id, t)));
        }

        document.querySelectorAll('#tournamentsTabsEl .tab-item').forEach(t => t.onclick = e => { 
            document.querySelectorAll('#tournamentsTabsEl .tab-item').forEach(x=>x.classList.remove('active'));
            e.currentTarget.classList.add('active'); 
            filterTournaments(currentTournamentGameId, currentTournamentModeId, e.currentTarget.dataset.status); 
        });
        
        function filterTournaments(gameId, modeId, status) {
            const cont = document.getElementById('tournamentsListContainerEl'); 
            if(!cont) return;
            cont.classList.remove('placeholder-glow'); getEl('noTournamentsMessageEl').style.display='none';
            const tArray = Object.entries(allTournamentsData).filter(([,t]) => {
                if(t.gameId !== gameId) return false;
                let statusMatch = (status === 'completed') ? (t.status === 'completed' || t.status === 'result' || t.status === 'canceled') : (t.status === status);
                if (!statusMatch) return false;
                if (modeId && t.modeId && t.modeId !== modeId) return false;
                return true;
            });
            (status === 'completed') ? tArray.sort(([,a],[,b]) => (b.startTime||0) - (a.startTime||0)) : tArray.sort(([,a],[,b]) => (a.startTime||0) - (b.startTime||0));
            cont.innerHTML = ''; 
            if(tArray.length > 0) tArray.forEach(([id, t]) => cont.appendChild(createCard(id, t))); 
            else getEl('noTournamentsMessageEl').style.display='block';
        }

        function createCard(id, t) {
            const card = document.createElement('div'); card.className = 'tournament-card';
            const eFee = t.entryFee || 0, maxP = t.maxPlayers || 0, regC = Object.keys(t.registeredPlayers || {}).length, isJ = currentUser && userProfile?.joinedTournaments?.[id];
            const displayMatchId = t.matchId ? t.matchId : `MATCH_${id.substring(id.length - 6).toUpperCase()}`;
            const gName = t.gameName || allGames[t.gameId]?.name || 'Game';
            const mName = t.modeName || allModes[t.modeId]?.modeName || allModes[t.modeId]?.name || 'Match';

            let btn = '', ipBtn = '', watchLiveBtn = '';
            
            if (t.liveStreamUrl && t.showLiveButton !== false) {
                watchLiveBtn = `<button class="btn-custom btn-primary-gradient flex-fill btn-watch-live w-100 mb-2" data-url="${t.liveStreamUrl}" style="background: linear-gradient(135deg, #ef4444, #991b1b); border:1px solid #ef4444; color:white;"><i class="bi bi-youtube fs-5"></i> ${t.liveStreamTitle || 'Watch Live'}</button>`;
            }

            if (t.status === 'completed' || t.status === 'result') { 
                btn = `<button class="btn-custom btn-outline-custom" disabled>Completed</button>`; 
                ipBtn = `<button class="btn-custom btn-primary-gradient mt-2 w-100 btn-results" data-id="${id}">View Results</button>`; 
            }
            else if (t.status === 'canceled') {
                btn = `<button class="btn-custom btn-outline-custom text-danger" style="border-color: #ef4444;" disabled>Canceled</button>`;
            }
            else if(isJ) { 
                btn = `<button class="btn-custom" style="background: rgba(16, 185, 129, 0.15); color: #10b981; border: 1px solid #10b981;" disabled>Joined</button>`; 
                if(['ongoing','upcoming'].includes(t.status)) ipBtn = `<button class="btn-custom btn-primary-gradient mt-2 w-100 btn-idpass" data-id="${id}">Room ID & Pass</button>`; 
            }
            else if(t.status === 'upcoming') {
                if (maxP === 0 || maxP - regC > 0) { btn = `<button class="btn-custom btn-primary-gradient btn-join btn-hover-glow" data-id="${id}">${window.FMT_C(eFee)} Join</button>`; } 
                else { btn = `<button class="btn-custom btn-outline-custom text-danger" style="border-color: #ef4444;" disabled>Match Full</button>`; }
            }
            else { btn = `<button class="btn-custom btn-outline-custom" disabled>Closed</button>`; }

            card.innerHTML = `
                <img src="${t.bannerUrl || 'https://via.placeholder.com/400x200'}" class="tournament-banner-image">
                <div class="tournament-card-content">
                    <div class="position-absolute d-flex gap-2" style="top:10px; left:10px;">
                        <span style="background: rgba(0,0,0,0.8); backdrop-filter: blur(5px); color: white; font-size: 0.7rem; font-weight: 800; padding: 4px 10px; border-radius: 6px; border: 1px solid rgba(255,255,255,0.2); text-transform: uppercase;">${t.mode||'Solo'}</span>
                        ${t.map?`<span style="background: rgba(0,0,0,0.8); backdrop-filter: blur(5px); color: white; font-size: 0.7rem; font-weight: 800; padding: 4px 10px; border-radius: 6px; border: 1px solid rgba(255,255,255,0.2); text-transform: uppercase;">${t.map}</span>`:''}
                    </div>
                    <div class="d-flex justify-content-between align-items-start mb-2">
                        <h3 class="fw-bold m-0 text-uppercase" style="font-size: 1.1rem; width: 65%; color: var(--text-heading, var(--text-main)); line-height: 1.2;">${t.name}</h3>
                        <div style="background:rgba(239,68,68,0.15); color:#ef4444; font-size:0.75rem; font-weight:800; padding:4px 8px; border-radius:8px; box-shadow: 0 0 10px rgba(239,68,68,0.2);">${t.status==='upcoming'?getTimeRemaining(t.startTime):t.status}</div>
                    </div>
                    <div class="d-flex justify-content-between rounded-3 p-3 mb-2" style="background: rgba(128,128,128,0.1); border: 1px solid var(--border-glass);">
                        <div class="text-center flex-fill border-end border-secondary prize-click-area d-flex flex-column justify-content-center align-items-center">
                            <span>Prize <i class="bi bi-info-circle small text-muted"></i></span>
                            <strong class="d-flex align-items-center glow-text fs-6 mt-1" style="color:var(--accent-gold);">${window.FMT_C(t.prizePool)}</strong>
                        </div>
                        <div class="text-center flex-fill border-end border-secondary d-flex flex-column justify-content-center align-items-center">
                            <span>Per Kill</span>
                            <strong class="d-flex align-items-center glow-text fs-6 mt-1" style="color:var(--accent-cyan);">${window.FMT_C(t.perKillPrize)}</strong>
                        </div>
                        <div class="text-center flex-fill d-flex flex-column justify-content-center align-items-center">
                            <span>Entry</span>
                            <strong class="d-flex align-items-center text-main fs-6 mt-1">${eFee>0?window.FMT_C(eFee):'Free'}</strong>
                        </div>
                    </div>
                    <div class="d-flex justify-content-between rounded-3 p-2 mb-3" style="background: rgba(128,128,128,0.05); border: 1px solid var(--border-glass); font-size: 0.75rem;">
                        <div class="text-start"><span class="text-muted fw-bold">Match ID:</span> <strong style="color:var(--text-main); letter-spacing:0.5px;">${displayMatchId}</strong></div>
                        <div class="text-end"><span class="text-muted fw-bold">Type:</span> <strong style="color:var(--accent-cyan); letter-spacing:0.5px;">${gName} - ${mName}</strong></div>
                    </div>
                    <div class="d-flex gap-2 flex-wrap">
                        ${watchLiveBtn}
                    </div>
                    <div class="d-flex gap-2">
                        <button class="btn-custom btn-outline-custom flex-fill btn-details">Details</button>
                        ${btn}
                    </div>
                    ${ipBtn}
                </div>`;
            
            card.querySelector('.btn-watch-live')?.addEventListener('click', (e) => { window.open(e.currentTarget.dataset.url, '_blank'); });

            card.querySelector('.prize-click-area')?.addEventListener('click', () => {
                const mBody = getEl('prizeListModalBodyEl'); let html = '';
                if (t.prizeList && Object.keys(t.prizeList).length > 0) {
                    const sortedRanks = Object.entries(t.prizeList).sort((a,b) => Number(a[0]) - Number(b[0]));
                    html += `<div class="list-group list-group-flush rounded-bottom" style="border-radius: 0 0 var(--radius-lg) var(--radius-lg); overflow:hidden;">`;
                    sortedRanks.forEach(([rank, amt]) => {
                        let badge = `${rank}th Prize`; let icon = '🏅';
                        if(rank == 1) { badge = '1st Prize'; icon = '🥇'; } else if(rank == 2) { badge = '2nd Prize'; icon = '🥈'; } else if(rank == 3) { badge = '3rd Prize'; icon = '🥉'; }
                        html += `<div class="list-group-item d-flex justify-content-between align-items-center bg-transparent border-bottom border-glass px-3 py-3 last-border-none"><span class="fw-bold text-main">${icon} ${badge}</span><strong class="glow-text d-flex align-items-center" style="color:var(--accent-gold); font-size:1.15rem;">${window.FMT_C(amt)}</strong></div>`;
                    });
                    html += `</div>`;
                } else { html = `<div class="p-4 text-center"><h5 class="fw-bold mb-2 text-main text-uppercase">Total Prize Pool</h5><h2 class="glow-text mb-0 d-flex justify-content-center align-items-center" style="color:var(--accent-gold); font-size: 2.2rem;">${window.FMT_C(t.prizePool)}</h2></div>`; }
                mBody.innerHTML = html; modals.prizeList.show();
            });

            // ESPORTS SLOT SELECTION SYSTEM
            card.querySelector('.btn-join')?.addEventListener('click', () => { 
                getEl('dynamicPlayerInputsContainer').innerHTML = '';
                getEl('joinTournamentIdInput').value = id; 
                
                let tMode = (t.mode || 'Solo').toLowerCase();
                let teamSize = 1;
                if (tMode === 'duo') teamSize = 2;
                else if (tMode === '3 player' || tMode === 'trio') teamSize = 3;
                else if (tMode === 'squad') teamSize = 4;
                
                getEl('joinTournamentForm').dataset.teamSize = teamSize;
                getEl('joinFeeDisplayEl').innerHTML = window.FMT_C(eFee * teamSize); 

                let inputsHTML = '';
                for(let i=1; i<=teamSize; i++) {
                    let pLabel = teamSize === 1 ? 'Player' : `Player ${i}`;
                    inputsHTML += `
                    <div class="p-3 mb-3 rounded-3" style="background: rgba(128,128,128,0.05); border: 1px solid var(--border-glass);">
                        <h6 class="text-start fw-bold mb-3" style="color: var(--accent-cyan); font-size: 0.85rem; text-transform: uppercase;"><i class="bi bi-person-fill me-1"></i> ${pLabel} Details</h6>
                        <div class="mb-3">
                            <label class="form-label text-start d-block">Game Name / IGN</label>
                            <input type="text" class="form-control player-name-input" id="pName_${i}" placeholder="Enter Exact Game Name" required>
                        </div>
                        <div class="mb-1">
                            <label class="form-label text-start d-block">Game UID / ID</label>
                            <input type="text" class="form-control player-uid-input" id="pUid_${i}" placeholder="Enter Exact Game UID" required>
                        </div>
                    </div>`;
                }

                let slotUI = `<div class="mt-3 p-3 rounded-3" style="background: rgba(128,128,128,0.05); border: 1px solid var(--border-glass);">
                    <div class="d-flex justify-content-between align-items-center mb-3">
                        <h6 class="text-start fw-bold m-0" style="color: var(--accent-cyan); font-size: 0.85rem; text-transform: uppercase;"><i class="bi bi-grid-3x3-gap-fill me-1"></i> Select Slots (${teamSize})</h6>
                        <small class="text-muted" style="font-size: 0.65rem;">Tap to Select</small>
                    </div>`;
                
                const bookedSlots = [];
                if (t.registeredPlayers) {
                    Object.values(t.registeredPlayers).forEach(rp => { 
                        if(rp.slots) rp.slots.forEach(s => bookedSlots.push(String(s)));
                        else if(rp.slot) bookedSlots.push(String(rp.slot)); 
                    });
                }
                const totalSlots = t.maxPlayers || 100;

                if (teamSize === 1) {
                    slotUI += `<div class="solo-slot-grid">`;
                    for(let s=1; s<=totalSlots; s++) {
                        const sId = String(s);
                        const isBooked = bookedSlots.includes(sId);
                        slotUI += `<div class="slot-item ${isBooked ? 'slot-booked' : 'slot-available'}" data-slot="${sId}">${sId}</div>`;
                    }
                    slotUI += `</div>`;
                } else {
                    slotUI += `<div class="esports-slot-grid">`;
                    const numTeams = Math.ceil(totalSlots / teamSize);
                    const chars = ['A', 'B', 'C', 'D'];
                    for(let i=1; i<=numTeams; i++) {
                        let teamHTML = `<div class="esports-slots">`;
                        let teamBookedCount = 0;
                        for(let j=0; j<teamSize; j++) {
                            const sId = `${i}${chars[j]}`;
                            const isBooked = bookedSlots.includes(sId);
                            if(isBooked) teamBookedCount++;
                            teamHTML += `<div class="slot-item ${isBooked ? 'slot-booked' : 'slot-available'}" data-slot="${sId}">${chars[j]}</div>`;
                        }
                        teamHTML += `</div>`;
                        const isTeamFull = (teamBookedCount === teamSize);
                        slotUI += `<div class="esports-team-row ${isTeamFull ? 'team-full' : ''}">
                            <div class="esports-team-name">Team ${i}</div>
                            ${teamHTML}
                        </div>`;
                    }
                    slotUI += `</div>`;
                }

                slotUI += `<input type="hidden" id="selectedSlotInput" required></div>`;
                inputsHTML += slotUI;
                getEl('dynamicPlayerInputsContainer').innerHTML = inputsHTML; 

                setTimeout(() => {
                    let selectedSlots = [];
                    document.querySelectorAll('.slot-available').forEach(btn => {
                        btn.onclick = function() {
                            let slotVal = this.dataset.slot;
                            if(selectedSlots.includes(slotVal)) {
                                selectedSlots = selectedSlots.filter(s => s !== slotVal);
                                this.classList.remove('slot-selected');
                                this.classList.add('slot-available');
                            } else {
                                if(selectedSlots.length >= teamSize) {
                                    showToast(`You can only select ${teamSize} slot(s)`, 'error');
                                    return;
                                }
                                selectedSlots.push(slotVal);
                                this.classList.remove('slot-available');
                                this.classList.add('slot-selected');
                            }
                            const slotInput = document.getElementById('selectedSlotInput');
                            if(slotInput) slotInput.value = JSON.stringify(selectedSlots);
                        }
                    });
                }, 100);

                modals.join.show(); 
            });

            card.querySelector('.btn-details')?.addEventListener('click', () => { 
                getEl('matchDetailsModalTitleEl').textContent = t.name;
                const mBody = getEl('matchDetailsModalBodyEl');
                
                let streamMarkup = '';
                if (t.liveStreamUrl && t.showLiveButton !== false) {
                    streamMarkup = `<br><button class="btn btn-danger w-100 fw-bold mt-2 py-2" onclick="window.open('${t.liveStreamUrl}', '_blank')" style="border-radius:12px;"><i class="bi bi-play-circle-fill"></i> ${t.liveStreamTitle || 'Watch Live Match'}</button>`;
                }

                const maxSlots = t.maxPlayers || 100;
                const bookedSlotsCount = Object.keys(t.registeredPlayers || {}).reduce((acc, curr) => {
                    const p = t.registeredPlayers[curr];
                    if(p.slots) return acc + p.slots.length;
                    return acc + 1;
                }, 0);
                const remainingSlots = maxSlots - bookedSlotsCount;

                let statsGrid = `
                <div class="row g-2 text-center mb-3">
                    <div class="col-6"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block text-uppercase fw-bold">Game</span><strong class="text-main">${gName}</strong></div></div>
                    <div class="col-6"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block text-uppercase fw-bold">Mode</span><strong class="text-main">${mName}</strong></div></div>
                    <div class="col-6"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block text-uppercase fw-bold">Entry Fee</span><strong class="text-success">${eFee>0 ? window.FMT_C(eFee) : 'Free'}</strong></div></div>
                    <div class="col-6"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block text-uppercase fw-bold">Prize Pool</span><strong class="text-warning glow-text">${window.FMT_C(t.prizePool)}</strong></div></div>
                    <div class="col-12"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block text-uppercase fw-bold">Start Time</span><strong class="text-main font-monospace">${formatDate(t.startTime)}</strong></div></div>
                </div>
                <div class="d-flex justify-content-between mb-3 text-muted small fw-bold px-1">
                    <span>Total Slots: <strong class="text-main">${maxSlots}</strong></span>
                    <span>Booked: <strong class="text-main">${bookedSlotsCount}</strong></span>
                    <span>Available: <strong class="text-main">${remainingSlots}</strong></span>
                </div>
                <div class="mb-3 p-2 text-center rounded" style="background: rgba(6, 182, 212, 0.1); border: 1px dashed var(--accent-cyan);">
                    <span class="text-muted fw-bold small text-uppercase">Match Status: </span> <strong class="text-main text-uppercase">${t.status}</strong>
                </div>`;

                let prizeMarkup = '';
                if (t.prizeList) {
                    prizeMarkup += `<div class="mt-4"><h6 class="fw-bold text-gradient mb-3" style="font-size:1.1rem;">🏆 Prize Distribution</h6><div class="glass-card p-0 overflow-hidden">`;
                    const sortedRanks = Object.entries(t.prizeList).sort((a,b) => Number(a[0]) - Number(b[0]));
                    sortedRanks.forEach(([rank, amt]) => {
                        let badge = `${rank}th Rank`;
                        if(rank == 1) badge = '🥇 1st Winner';
                        else if(rank == 2) badge = '🥈 2nd Winner';
                        else if(rank == 3) badge = '🥉 3rd Winner';
                        prizeMarkup += `<div class="d-flex justify-content-between align-items-center p-3 border-bottom border-glass last-border-none"><span class="fw-bold text-main">${badge}</span><strong style="color:var(--accent-gold); font-size:1.1rem;" class="glow-text d-flex align-items-center">${window.FMT_C(amt)}</strong></div>`;
                    });
                    prizeMarkup += `</div></div>`;
                }

                mBody.innerHTML = `${statsGrid}<h6 class="fw-bold text-gradient mb-2 mt-4" style="font-size:1.1rem;"><i class="bi bi-file-earmark-text"></i> Rules & Details</h6><div class="p-3 rounded" style="background:rgba(128,128,128,0.05); border:1px solid var(--border-glass);"><p class="m-0">${t.description || 'No special rules provided.'}</p></div>${prizeMarkup}${streamMarkup}`;
                modals.matchDetails.show();
            });

            card.querySelector('.btn-idpass')?.addEventListener('click', () => { getEl('roomIdDisplayEl').textContent = t.roomId || 'Waiting...'; getEl('roomPasswordDisplayEl').textContent = t.roomPassword || 'Waiting...'; modals.idPass.show(); });
            card.querySelector('.btn-results')?.addEventListener('click', () => { 
                getEl('matchDetailsModalTitleEl').textContent = "Results - " + t.name; 
                let personalSummary = '';
                const myReg = currentUser && t.registeredPlayers?.[currentUser.uid];
                if (myReg) {
                    const wonAmt = (Number(myReg.prize)||0) + (Number(myReg.extraPrize)||0) + (Number(myReg.bonus)||0);
                    const slotDisp = myReg.slots ? myReg.slots.join(', ') : (myReg.slot || 'N/A');
                    personalSummary = `
                    <div class="row g-2 text-center mb-3">
                        <div class="col-4"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block fw-bold">Rank</span><strong class="text-main">${myReg.rank || '-'}</strong></div></div>
                        <div class="col-4"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block fw-bold">Kills</span><strong class="text-main">${myReg.kills || 0}</strong></div></div>
                        <div class="col-4"><div class="p-2 glass-card m-0 border-0" style="background: rgba(128,128,128,0.1);"><span class="small text-muted d-block fw-bold">Won</span><strong style="color:#10b981;">${window.FMT_C(wonAmt)}</strong></div></div>
                    </div>
                    <div class="p-2 rounded mb-3 text-center small" style="background: rgba(128,128,128,0.08);">Slot(s): <strong class="text-main">${slotDisp}</strong></div>`;
                }
                let resultsStream = t.liveStreamUrl ? `<a href="${t.liveStreamUrl}" target="_blank" class="btn btn-danger w-100 fw-bold mt-3 py-2" style="border-radius:12px;"><i class="bi bi-youtube"></i> Highlights / VOD</a>` : '';
                getEl('matchDetailsModalBodyEl').innerHTML = `${personalSummary}<p class="text-muted mb-0">Check Profile -> Match History for full match details and scoreboards.</p>${resultsStream}`; 
                modals.matchDetails.show(); 
            });
            return card;
        }

        // ================= MATCH JOIN LOGIC (WITH TRANSACTION) =================
        getEl('confirmJoinBtn').onclick = async () => {
            const tid = getEl('joinTournamentIdInput').value;
            const tDat = allTournamentsData[tid];
            if(!tDat) return showToast("Tournament not found!", "error");
            if(tDat.status === 'canceled' || tDat.status === 'completed' || tDat.status === 'result') return showToast("Tournament closed", "error");

            const eFee = tDat.entryFee || 0;
            const teamSize = parseInt(getEl('joinTournamentForm').dataset.teamSize || 1);
            const totalFee = eFee * teamSize;
            
            let teamDetails = [];
            for(let i=1; i<=teamSize; i++) {
                let name = getEl(`pName_${i}`)?.value.trim() || '';
                let rawUid = getEl(`pUid_${i}`)?.value || '';
                let uid = String(rawUid).replace(/\s+/g, ''); 
                
                if(!name || name.length < 3 || name.length > 25) return showToast(`Player ${i} Name must be 3-25 characters`, "error");
                if(!uid || uid.length < 4 || uid.length > 25 || isNaN(uid)) return showToast(`Player ${i} UID must be a valid number`, "error");
                
                teamDetails.push({ gameName: name, gameUid: uid });
            }

            let selectedSlots = [];
            try { selectedSlots = JSON.parse(document.getElementById('selectedSlotInput')?.value || '[]'); } catch(e){}
            if(selectedSlots.length !== teamSize) return showToast(`Please select exactly ${teamSize} slots!`, "error");

            const p1Name = teamDetails[0].gameName;
            const p1Uid = teamDetails[0].gameUid;
            
            const safeUserName = safeStr(userProfile.displayName || userProfile.email?.split('@')[0], 'Unknown').trim();
            const safeUserEmail = safeStr(userProfile.email, 'Unknown').trim();

            if((Number(userProfile.balance)||0) + (Number(userProfile.winningCash)||0) < totalFee) return showToast("Insufficient Wallet Balance", "error");
            if(userProfile?.joinedTournaments?.[tid]) return showToast("You already joined this match!", "error");
            
            showLoader(true);
            try {
                // 1. Transaction to deduct balance safely
                const uRef = ref(db, `users/${currentUser.uid}`);
                const wTx = await runTransaction(uRef, (user) => {
                    if(!user) return user;
                    let uDep = Number(user.balance) || 0;
                    let uWin = Number(user.winningCash) || 0;
                    if(uDep + uWin < totalFee) return;
                    if(uDep >= totalFee) user.balance = uDep - totalFee;
                    else { user.balance = 0; user.winningCash = uWin - (totalFee - uDep); }
                    return user;
                });
                
                if(!wTx.committed) { showLoader(false); return showToast("Insufficient Wallet Balance", "error"); }

                let tModeEnum = 'Solo';
                if(teamSize == 2) tModeEnum = 'Duo';
                if(teamSize == 3) tModeEnum = 'Trio';
                if(teamSize == 4) tModeEnum = 'Squad';

                // 2. Transaction to securely book slots
                const rpRef = ref(db, `tournaments/${tid}/registeredPlayers`);
                const rpTx = await runTransaction(rpRef, (players) => {
                    if(players === null) players = {};
                    if(players[currentUser.uid]) return;

                    let booked = [];
                    Object.values(players).forEach(p => {
                        if(p.slots) p.slots.forEach(s => booked.push(String(s)));
                        else if(p.slot) booked.push(String(p.slot));
                    });

                    if(selectedSlots.some(s => booked.includes(String(s)))) return; 

                    players[currentUser.uid] = { 
                        timestamp: Date.now(), 
                        gameName: p1Name,       
                        gameUid: p1Uid,         
                        playerName: p1Name,     
                        playerUid: p1Uid,       
                        userName: safeUserName, 
                        userEmail: safeUserEmail,
                        userId: currentUser.uid,
                        matchId: tid,
                        teamMode: tModeEnum,
                        teamDetails: teamDetails,
                        slot: selectedSlots[0],
                        slots: selectedSlots,
                        matchStatus: 'playing'
                    };
                    return players;
                });

                if(!rpTx.committed) {
                    await runTransaction(uRef, (user) => {
                        if(user) user.balance = (Number(user.balance) || 0) + totalFee;
                        return user;
                    });
                    showLoader(false);
                    return showToast("Selected slot(s) already taken! Balance refunded.", "error");
                }

                await update(ref(db, `users/${currentUser.uid}/joinedTournaments/${tid}`), { timestamp: serverTimestamp() });
                
                await push(ref(db, `users/${currentUser.uid}/notifications`), {
                    title: "Match Joined Successfully",
                    message: `You successfully booked slot(s) [${selectedSlots.join(', ')}] in ${tDat.name}. Entry Fee: ${window.FMT_C(totalFee)}.`,
                    type: "success",
                    read: false,
                    timestamp: serverTimestamp()
                });

                modals.join.hide(); showToast("Joined Match Successfully!", "success"); showSection('home-section');
            } catch(e) { showToast(e.message, "error"); } finally { showLoader(false); }
        };

        // ================= RECHARGE / ADVANCED WITHDRAWAL =================
        let finalRechargeAmt = 0;
        getEl('addAmountWalletBtnEl').onclick = () => { showSection('recharge-section', 'wallet-section'); getEl('recharge-step-1-amount').style.display='block'; getEl('recharge-step-2-method').style.display='none'; getEl('recharge-step-3-manual').style.display='none'; };
        document.querySelectorAll('.amount-preset-btn').forEach(b => b.onclick = () => getEl('rechargeAmountInput').value = b.dataset.amount);
        
        getEl('goToStep2Btn').onclick = () => {
            finalRechargeAmt = parseFloat(getEl('rechargeAmountInput').value); const min = appSettings.payment?.min_deposit || 10, max = appSettings.payment?.max_deposit || 50000;
            if(!finalRechargeAmt || finalRechargeAmt < min || finalRechargeAmt > max) return showToast(`Amount must be ${min} - ${max}`, "error");
            getEl('rechargeAmountConfirm').textContent = finalRechargeAmt; getEl('recharge-step-1-amount').style.display='none'; getEl('recharge-step-2-method').style.display='block';
        };
        document.querySelectorAll('input[name="payType"]').forEach(r => r.addEventListener('change', function() { document.querySelectorAll('#optionAutoCard, #optionManualCard').forEach(c => {c.style.borderColor = 'var(--border-glass)'; c.style.background = 'transparent';}); this.closest('.glass-card').style.borderColor = 'var(--accent-cyan)'; this.closest('.glass-card').style.background = 'rgba(128,128,128,0.1)'; }));

        getEl('proceedToPayActionBtn').onclick = () => {
            const typeEl = document.querySelector('input[name="payType"]:checked');
            const type = typeEl ? typeEl.value : 'manual';
            if(type === 'auto') {
                const zkey = appSettings.payment?.zap_key;
                if(!appSettings.payment?.gateway_enabled || !zkey || typeof ZapUPI === 'undefined') return showToast('Gateway disabled. Use Manual.', 'error');
                showLoader(true);
                const oid = "ORD" + Date.now();
                ZapUPI.createOrder({ zap_key: zkey, order_id: oid, amount: finalRechargeAmt.toString(), remark: `UID:${currentUser.uid}` }, {
                    onResponse: (url, rOid) => { set(ref(db, `orders/${rOid}`), { userId: currentUser.uid, amount: finalRechargeAmt, status: 'pending', timestamp: serverTimestamp() }).then(() => { showLoader(false); ZapUPI.loadPayment(url); }).catch(() => { showLoader(false); showToast("Sync failed", "error"); }); },
                    onError: err => { showLoader(false); showToast(err, "error"); }
                });
            } else {
                getEl('recharge-step-2-method').style.display = 'none'; getEl('recharge-step-3-manual').style.display = 'block';
                getEl('rechargeFinalAmount').textContent = finalRechargeAmt; getEl('rechargeUpiId').textContent = appSettings.upiDetails || 'admin@upi'; getEl('rechargeQrCodeImg').src = appSettings.qrCodeUrl || 'https://via.placeholder.com/150';
            }
        };

        getEl('rechargeSubmitBtn').onclick = async () => {
            const utr = getEl('rechargeUtrInput').value; if(!utr) return showToast("Enter UTR", "error");
            showLoader(true); try { await push(ref(db, 'deposits'), { userId: currentUser.uid, amount: finalRechargeAmt, utr: utr, status: 'pending', paymentMethod: 'Manual UPI', timestamp: serverTimestamp() }); showToast("Deposit Requested", "success"); showSection('wallet-section'); } catch(e) {} showLoader(false);
        };

        getEl('checkZapStatusBtn').onclick = () => {
            if (typeof ZapUPI === 'undefined') return showToast('Payment SDK unavailable', 'error');
            const oid = getEl('statusCheckOrderId').value.trim(), zkey = appSettings.payment?.zap_key;
            if(!oid || !zkey) return showToast('Missing info', 'error');
            showLoader(true);
            ZapUPI.orderStatus({ zap_key: zkey, order_id: oid }, {
                onResponse: (rOid, data) => { showLoader(false); const d = data.data; if(!d) return showToast('Not found', 'error');
                    getEl('statusCheckResult').style.display = 'block'; getEl('statusCheckResult').innerHTML = `<div class="mb-2"><strong>ID:</strong> ${d.order_id}</div><div class="mb-2"><strong>Status:</strong> ${d.status}</div><div><strong>Txn:</strong> ${d.txn_id || '-'}</div>`;
                }, onError: () => { showLoader(false); showToast('Check failed', 'error'); }
            });
        };

        document.querySelectorAll('.wd-tab-btn').forEach(btn => {
            btn.addEventListener('click', (e) => {
                document.querySelectorAll('.wd-tab-btn').forEach(b => { b.classList.remove('active'); b.style.background = 'transparent'; b.style.color = 'var(--text-muted)'; });
                e.currentTarget.classList.add('active'); e.currentTarget.style.background = 'var(--bg-card)'; e.currentTarget.style.color = 'var(--text-main)';
                if (e.currentTarget.dataset.type === 'money') { getEl('wdMoneySection').style.display = 'block'; getEl('wdRedeemSection').style.display = 'none'; } 
                else { getEl('wdMoneySection').style.display = 'none'; getEl('wdRedeemSection').style.display = 'block'; }
            });
        });

        getEl('withdrawBtnEl').onclick = () => { getEl('withdrawModalBalanceEl').innerHTML = window.FMT_C((Number(userProfile.winningCash)||0).toFixed(2)); modals.withdraw.show(); };
        
        getEl('submitWithdrawRequestBtnEl').onclick = async () => {
            const wdType = document.querySelector('.wd-tab-btn.active')?.dataset.type || 'money';
            const min = appSettings.minWithdraw || 50;

            if (wdType === 'money') {
                const amt = parseFloat(getEl('withdrawAmountInputEl').value);
                const det = getEl('withdrawMethodInputEl').value;
                if(!amt || amt < min) return showToast(`Min withdraw is ${min}`, 'error');
                if(!det) return showToast('Enter Bank/UPI', 'error');
                showLoader(true);
                try {
                    const tx = await runTransaction(ref(db, `users/${currentUser.uid}`), u => { if(u && Number(u.winningCash) >= amt) { u.winningCash = Number(u.winningCash) - amt; return u; } return; });
                    if(!tx.committed) throw new Error("Insufficient Balance");
                    await push(ref(db, 'withdrawals'), { userId: currentUser.uid, userEmail: userProfile.email, amount: amt, methodDetails: {accountInfo: det}, withdrawalType: 'money', status: 'pending', requestTimestamp: serverTimestamp() });
                    modals.withdraw.hide(); showToast("Withdrawal Requested", "success"); showSection('wallet-section'); getEl('withdrawAmountInputEl').value = ''; getEl('withdrawMethodInputEl').value = '';
                } catch(e) { showToast(e.message, "error"); } showLoader(false);
            } else {
                const amt = parseFloat(getEl('withdrawRedeemAmountInputEl').value);
                if(!amt || amt < min) return showToast(`Min redeem is ${min}`, 'error');
                showLoader(true);
                try {
                    const tx = await runTransaction(ref(db, `users/${currentUser.uid}`), u => { if(u && Number(u.winningCash) >= amt) { u.winningCash = Number(u.winningCash) - amt; return u; } return; });
                    if(!tx.committed) throw new Error("Insufficient Balance");
                    await push(ref(db, 'withdrawals'), { userId: currentUser.uid, userName: userProfile.displayName || 'User', userEmail: userProfile.email, amount: amt, withdrawalType: 'redeem', status: 'pending', requestTimestamp: serverTimestamp() });
                    modals.withdraw.hide(); showToast("Redeem Code Requested", "success"); showSection('wallet-section'); getEl('withdrawRedeemAmountInputEl').value = '';
                } catch(e) { showToast(e.message, "error"); } showLoader(false);
            }
        };

        // ================= MATCH HISTORY =================
        function loadMatchHistory() {
            const body = document.getElementById('matchHistoryBodyEl'); 
            body.innerHTML = '<div class="text-center py-4"><div class="spinner-border glow-text" style="color:var(--accent-cyan);"></div></div>';
            
            const myM = Object.entries(allTournamentsData).filter(([,t]) => t.registeredPlayers?.[currentUser.uid]).sort(([,a], [,b]) => (b.startTime||0) - (a.startTime||0));
            
            if(myM.length===0) {
                body.innerHTML = '<p class="text-center text-muted py-4 fw-bold">No matches played yet.</p>';
                return;
            }
            
            let hHTML = '';
            myM.forEach(([,t]) => {
                const st = t.registeredPlayers[currentUser.uid];
                const gName = allGames[t.gameId]?.name || 'Game';
                const mName = allModes[t.modeId]?.name || 'Mode';
                const slotDisp = st.slots ? st.slots.join(', ') : (st.slot || 'N/A');
                let teamStr = '';
                if(st.slots && st.slots.length > 0) { const match = String(st.slots[0]).match(/\d+/); if(match) teamStr = `<br><span class="small text-muted">Team No: <strong class="text-white">${match[0]}</strong></span>`; }
                
                let statusBadge = '';
                const ms = st.matchStatus || 'playing';
                if(ms === 'winner') statusBadge = '<span class="badge bg-success"><i class="bi bi-trophy-fill"></i> Winner</span>';
                else if(ms === 'loser') statusBadge = '<span class="badge bg-danger">Defeated</span>';
                else if(ms === 'disqualified') statusBadge = '<span class="badge bg-warning text-dark">Disqualified</span>';
                else statusBadge = '<span class="badge bg-info text-dark">Playing</span>';
                
                const tStat = t.status === 'result' ? 'COMPLETED' : (t.status || 'UPCOMING').toUpperCase();

                hHTML += `<div class="glass-card p-3 mb-3 border-start border-4" style="border-color: var(--accent-cyan) !important;">
                    <div class="d-flex justify-content-between mb-2 align-items-start">
                        <div>
                            <h6 class="fw-bold m-0 text-main">${t.name}</h6>
                            <span class="small text-muted">${gName} - ${mName}</span>
                        </div>
                        <span class="badge" style="font-size:0.65rem; background: rgba(0,255,255,0.15); color: #00ffff; border: 1px solid rgba(0,255,255,0.4);">${tStat}</span>
                    </div>
                    <div class="d-flex justify-content-between my-2 p-2 rounded" style="background: rgba(128,128,128,0.1);">
                        <div><span class="small text-muted d-block">Slot(s)</span><strong class="text-white">${slotDisp}</strong>${teamStr}</div>
                        <div class="text-center"><span class="small text-muted d-block">Entry Fee</span><strong class="text-white">${t.entryFee>0?window.FMT_C(t.entryFee):'Free'}</strong></div>
                        <div class="text-end"><span class="small text-muted d-block">Result Status</span>${statusBadge}</div>
                    </div>
                    <div class="d-flex justify-content-between small text-muted pt-2 border-top border-secondary">
                        <span>Rank: <strong class="text-main">${st.rank||'-'}</strong></span>
                        <span>Kills: <strong class="text-main">${st.kills||0}</strong></span>
                        <span class="d-flex align-items-center">Won: <strong class="ms-1 d-flex align-items-center" style="color:#10b981;">${window.FMT_C((Number(st.prize)||0)+(Number(st.extraPrize)||0)+(Number(st.bonus)||0))}</strong></span>
                    </div>
                </div>`;
            }); 
            body.innerHTML = hHTML;
            applyCurrencySymbol();
        }

        // ================= NOTIFICATION ENGINE =================
        function listenToNotifications() {
            if(!currentUser) return;
            const uNotifsRef = ref(db, `users/${currentUser.uid}/notifications`);
            const gNotifsRef = ref(db, 'globalNotifications');
            
            if(activeUserNotifsListener) { off(uNotifsRef, 'value', activeUserNotifsListener.callback); }
            if(activeGlobalNotifsListener) { off(gNotifsRef, 'value', activeGlobalNotifsListener.callback); }

            let userNotifs = [];
            let globalNotifs = [];

            const renderBadge = () => {
                let unreadCount = 0;
                let readGlobalNotifs = JSON.parse(localStorage.getItem('readGlobalNotifs') || '[]');
                
                fetchedNotifs.forEach(n => {
                    if(n.isGlobal && !readGlobalNotifs.includes(n.id)) unreadCount++;
                    if(!n.isGlobal && n.read !== true) unreadCount++;
                });
                
                const badge = getEl('notificationBadgeEl');
                if(badge.tagName) {
                    badge.textContent = unreadCount;
                    badge.style.display = unreadCount > 0 ? 'flex' : 'none';
                }
                
                if (document.getElementById("notificationOverlay").classList.contains("show")) {
                    renderNotificationsList();
                }
            };

            const updateCombined = () => {
                fetchedNotifs = [...userNotifs, ...globalNotifs];
                fetchedNotifs.sort((a,b) => (b.timestamp||0) - (a.timestamp||0)); 
                renderBadge();
            };

            const userCb = onValue(uNotifsRef, snap => {
                userNotifs = [];
                if(snap.exists()) { snap.forEach(c => { userNotifs.push({...c.val(), id: c.key, isGlobal: false}); }); }
                updateCombined();
            });
            activeUserNotifsListener = { ref: uNotifsRef, callback: userCb };

            const globalCb = onValue(gNotifsRef, snap => {
                globalNotifs = [];
                if(snap.exists()) { snap.forEach(c => { globalNotifs.push({...c.val(), id: c.key, isGlobal: true}); }); }
                updateCombined();
            });
            activeGlobalNotifsListener = { ref: gNotifsRef, callback: globalCb };
        }

        window.renderNotificationsList = function() {
            const list = document.getElementById('notificationsListEl');
            const emp = document.getElementById('notificationsEmptyMsgEl');
            list.innerHTML=''; emp.style.display='none';
            
            if(fetchedNotifs.length===0) { emp.style.display='block'; return; }
            
            let readGlobalNotifs = JSON.parse(localStorage.getItem('readGlobalNotifs') || '[]');
            let globalsUpdated = false;

            fetchedNotifs.forEach(n => {
                let iconCol = n.type === 'error' ? '#ef4444' : (n.type === 'success' ? '#10b981' : (n.type === 'info' ? 'var(--accent-cyan)' : 'var(--accent-gold)'));
                let icon = n.type === 'error' ? 'bi-x-circle-fill' : (n.type === 'success' ? 'bi-check-circle-fill' : 'bi-bell-fill');
                
                list.innerHTML += `<div class="glass-card p-3 mb-2 border-start border-4" style="border-color:${iconCol} !important;">
                    <div class="d-flex justify-content-between align-items-center mb-1">
                        <h6 class="fw-bold mb-0 text-main"><i class="bi ${icon} me-2" style="color:${iconCol};"></i>${n.title||'Update'}</h6>
                        <span style="font-size:0.65rem; color:var(--text-muted);">${formatDate(n.timestamp)}</span>
                    </div>
                    <p class="small text-muted m-0 mt-2" style="line-height:1.4;">${n.message}</p>
                </div>`;

                if(n.isGlobal && !readGlobalNotifs.includes(n.id)) {
                    readGlobalNotifs.push(n.id);
                    globalsUpdated = true;
                } else if(!n.isGlobal && n.read !== true) {
                    update(ref(db, `users/${currentUser.uid}/notifications/${n.id}`), {read: true});
                }
            });

            if(globalsUpdated) localStorage.setItem('readGlobalNotifs', JSON.stringify(readGlobalNotifs));
            getEl('notificationBadgeEl').style.display = 'none';
        }

        getEl('editNameBtnEl').onclick = () => { getEl('editNameInput').value = userProfile.displayName || ''; getEl('editPasswordInput').value = ''; modals.editName.show(); };
        getEl('saveNameChangeBtn').onclick = async () => {
            const nn = getEl('editNameInput').value.trim(), np = getEl('editPasswordInput').value;
            if(!nn) return showToast('Name required', 'error');
            showLoader(true); try { await update(ref(db, `users/${currentUser.uid}`), { displayName: nn }); if(np.length>0) { if(np.length<6) throw new Error("Pass min 6"); await updatePassword(currentUser, np); } showToast("Updated", "success"); modals.editName.hide(); } catch(e) { showToast(e.message, "error"); } showLoader(false);
        };

        async function loadLeaderboard() {
            const list = document.getElementById('leaderboardListEl'); list.innerHTML = '<div class="text-center py-4"><div class="spinner-border glow-text" style="color:var(--accent-cyan);"></div></div>';
            try {
                const snap = await get(ref(db, 'users')); const users = [];
                snap.forEach(c => { const u=c.val(); if(u.leaderboardRank) users.push(u); });
                users.sort((a,b) => a.leaderboardRank - b.leaderboardRank); list.innerHTML = '';
                if(users.length === 0) return list.innerHTML = '<p class="text-center text-muted py-3 fw-bold">No ranking available.</p>';
                users.forEach((u, i) => { 
                    let tr = i===0?'🏆':(i===1?'🥈':(i===2?'🥉':`#${u.leaderboardRank}`)); 
                    let safeName = u.displayName || u.email?.split('@')[0] || 'Player';
                    list.innerHTML += `<div class="d-flex align-items-center justify-content-between p-3 border-bottom border-glass last-border-none"><div class="d-flex align-items-center gap-3"><h5 class="m-0 text-muted" style="width:30px;">${tr}</h5><img src="https://ui-avatars.com/api/?name=${encodeURIComponent(safeName)}&background=18181b&color=06b6d4&bold=true" style="width:40px;height:40px;border-radius:10px;"><h6 class="m-0 fw-bold text-main">${safeName}</h6></div><strong class="glow-text d-flex align-items-center" style="color:var(--accent-gold);">${window.FMT_C(u.leaderboardDisplayEarnings||0)}</strong></div>`; 
                });
            } catch(e) {}
        }
    </script>
</body>
</html>
