<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <title>NETHER AI | Premium Code Generation</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --bg-dark: #0a0a1a;
            --bg-darker: #050510;
            --text-primary: #ffffff;
            --text-secondary: #94a3b8;
            --accent: #818cf8;
            --success: #10b981;
            --error: #ef4444;
            --warning: #f59e0b;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--bg-darker);
            color: var(--text-primary);
            overflow-x: hidden;
            min-height: 100vh;
        }

        .grid-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(99, 102, 241, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(99, 102, 241, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: 0;
            pointer-events: none;
        }

        .emoji-float {
            position: fixed;
            font-size: 60px;
            opacity: 0.15;
            pointer-events: none;
            z-index: 0;
            animation: float-emoji 20s infinite ease-in-out;
            filter: blur(1px);
        }

        @keyframes float-emoji {
            0%, 100% { 
                transform: translate(0, 0) rotate(0deg);
            }
            25% { 
                transform: translate(40px, -40px) rotate(15deg);
            }
            50% { 
                transform: translate(-30px, 30px) rotate(-15deg);
            }
            75% { 
                transform: translate(30px, -20px) rotate(10deg);
            }
        }

        .emoji-1 { top: 10%; left: 5%; animation-delay: 0s; }
        .emoji-2 { top: 20%; right: 10%; animation-delay: 3s; }
        .emoji-3 { bottom: 15%; left: 15%; animation-delay: 6s; }
        .emoji-4 { bottom: 25%; right: 5%; animation-delay: 9s; }
        .emoji-5 { top: 50%; left: 50%; animation-delay: 4s; }
        .emoji-6 { top: 30%; left: 25%; animation-delay: 7s; }
        .emoji-7 { bottom: 40%; right: 30%; animation-delay: 2s; }
        .emoji-8 { top: 60%; left: 70%; animation-delay: 11s; }

        .container {
            position: relative;
            z-index: 1;
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            margin-bottom: 40px;
        }

        .logo {
            font-size: 24px;
            font-weight: 800;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--primary);
            -webkit-text-fill-color: var(--primary);
        }

        .logo-badge {
            font-size: 10px;
            background: var(--primary);
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-weight: 700;
        }

        .nav-buttons {
            display: flex;
            gap: 12px;
        }

        .nav-btn {
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: var(--text-primary);
            padding: 10px 20px;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-btn:hover {
            background: rgba(99, 102, 241, 0.2);
            border-color: var(--primary);
            transform: translateY(-2px);
        }

        .hero {
            text-align: center;
            padding: 60px 20px 80px;
            max-width: 900px;
            margin: 0 auto;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: var(--accent);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 30px;
        }

        .hero h1 {
            font-size: 56px;
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #ffffff, var(--text-secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 20px;
            color: var(--text-secondary);
            line-height: 1.6;
            margin-bottom: 40px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            padding: 16px 32px;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 700;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 10px 40px rgba(99, 102, 241, 0.3);
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 15px 50px rgba(99, 102, 241, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            padding: 16px 32px;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            border: 1px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .btn-secondary:hover {
            border-color: var(--primary);
            background: rgba(99, 102, 241, 0.1);
        }

        .stats-bar {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 60px 0;
            padding: 40px;
            background: rgba(99, 102, 241, 0.05);
            border: 1px solid rgba(99, 102, 241, 0.1);
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .stat-item {
            text-align: center;
        }

        .stat-value {
            font-size: 36px;
            font-weight: 900;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 8px;
        }

        .stat-label {
            font-size: 14px;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 600;
        }

        .workspace {
            background: rgba(10, 10, 26, 0.6);
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 24px;
            padding: 40px;
            backdrop-filter: blur(20px);
            margin-bottom: 40px;
            position: relative;
        }

        .workspace-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }

        .workspace-title {
            font-size: 20px;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .workspace-title i {
            color: var(--primary);
        }

        .workspace-status {
            font-size: 12px;
            background: rgba(16, 185, 129, 0.1);
            border: 1px solid rgba(16, 185, 129, 0.3);
            color: var(--success);
            padding: 6px 12px;
            border-radius: 6px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .workspace-status.error {
            background: rgba(239, 68, 68, 0.1);
            border-color: rgba(239, 68, 68, 0.3);
            color: var(--error);
        }

        .tabs {
            display: flex;
            gap: 8px;
            margin-bottom: 30px;
            overflow-x: auto;
            padding-bottom: 10px;
        }

        .tabs::-webkit-scrollbar {
            height: 4px;
        }

        .tabs::-webkit-scrollbar-track {
            background: rgba(99, 102, 241, 0.1);
        }

        .tabs::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 2px;
        }

        .tab {
            background: transparent;
            border: 1px solid rgba(99, 102, 241, 0.2);
            color: var(--text-secondary);
            padding: 12px 24px;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            white-space: nowrap;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .tab:hover {
            border-color: var(--primary);
            color: var(--text-primary);
        }

        .tab.active {
            background: var(--primary);
            border-color: var(--primary);
            color: white;
            box-shadow: 0 4px 20px rgba(99, 102, 241, 0.4);
        }

        .editor-container {
            position: relative;
            background: #000000;
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 16px;
            overflow: hidden;
        }

        .editor-wrapper {
            position: relative;
            min-height: 400px;
            max-height: 600px;
            overflow: auto;
            padding-left: 50px;
        }

        .line-numbers {
            position: absolute;
            left: 0;
            top: 0;
            width: 50px;
            padding: 20px 10px;
            background: #0a0a1a;
            color: #666;
            font-family: 'JetBrains Mono', monospace;
            font-size: 14px;
            line-height: 1.8;
            text-align: right;
            user-select: none;
            border-right: 1px solid rgba(99, 102, 241, 0.2);
        }

        .editor {
            padding: 20px;
            font-family: 'JetBrains Mono', 'Fira Code', monospace;
            font-size: 14px;
            line-height: 1.8;
            color: #e2e8f0;
            white-space: pre-wrap;
            word-wrap: break-word;
            min-height: 400px;
            outline: none;
            background: transparent;
        }

        .editor::-webkit-scrollbar {
            width: 8px;
        }

        .editor::-webkit-scrollbar-track {
            background: #0a0a1a;
        }

        .editor::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }

        .kw { color: #ff79c6; font-weight: 600; }
        .fn { color: #50fa7b; }
        .str { color: #f1fa8c; }
        .cmt { color: #6272a4; font-style: italic; }
        .num { color: #bd93f9; }
        .var { color: #66d9ef; }
        .tag { color: #f92672; }

        .editor-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 20px;
            background: #0a0a1a;
            border-top: 1px solid rgba(99, 102, 241, 0.2);
            font-size: 12px;
            color: var(--text-secondary);
        }

        .editor-actions {
            display: flex;
            gap: 12px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .action-btn {
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: var(--text-primary);
            padding: 12px 24px;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .action-btn:hover {
            background: rgba(99, 102, 241, 0.2);
            border-color: var(--primary);
            transform: translateY(-2px);
        }

        .action-btn-primary {
            background: var(--primary);
            border-color: var(--primary);
        }

        .action-btn-primary:hover {
            background: var(--primary-dark);
        }

        .input-section {
            background: rgba(10, 10, 26, 0.6);
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 24px;
            padding: 30px;
            backdrop-filter: blur(20px);
            position: sticky;
            bottom: 20px;
        }

        .input-wrapper {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .input-field {
            flex: 1;
            background: #000000;
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: var(--text-primary);
            padding: 18px 24px;
            border-radius: 16px;
            font-size: 15px;
            font-weight: 500;
            resize: none;
            min-height: 60px;
            max-height: 150px;
            transition: all 0.3s ease;
        }

        .input-field:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
        }

        .input-field::placeholder {
            color: var(--text-secondary);
        }

        .send-btn {
            width: 60px;
            height: 60px;
            background: var(--primary);
            border: none;
            border-radius: 16px;
            color: white;
            font-size: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 40px rgba(99, 102, 241, 0.3);
        }

        .send-btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 15px 50px rgba(99, 102, 241, 0.4);
        }

        .send-btn:active {
            transform: scale(0.95);
        }

        .send-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none;
        }

        .templates {
            display: flex;
            gap: 10px;
            margin-top: 15px;
            overflow-x: auto;
            padding-bottom: 10px;
        }

        .template-btn {
            background: transparent;
            border: 1px solid rgba(99, 102, 241, 0.2);
            color: var(--text-secondary);
            padding: 8px 16px;
            border-radius: 8px;
            font-size: 12px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            white-space: nowrap;
        }

        .template-btn:hover {
            border-color: var(--primary);
            color: var(--text-primary);
            background: rgba(99, 102, 241, 0.1);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            z-index: 1000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal.show {
            display: flex;
        }

        .modal-content {
            background: var(--bg-dark);
            border: 1px solid rgba(99, 102, 241, 0.3);
            border-radius: 24px;
            padding: 40px;
            max-width: 600px;
            width: 100%;
            max-height: 80vh;
            overflow-y: auto;
            animation: modalSlideUp 0.3s ease;
        }

        @keyframes modalSlideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .modal-header {
            font-size: 24px;
            font-weight: 800;
            margin-bottom: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-close {
            cursor: pointer;
            font-size: 28px;
            color: var(--text-secondary);
            transition: all 0.3s ease;
        }

        .modal-close:hover {
            color: var(--error);
            transform: rotate(90deg);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-label {
            display: block;
            font-size: 13px;
            font-weight: 600;
            color: var(--text-secondary);
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .form-input {
            width: 100%;
            background: #000000;
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: var(--text-primary);
            padding: 14px 18px;
            border-radius: 12px;
            font-size: 14px;
            transition: all 0.3s ease;
        }

        .form-input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
        }

        .form-help {
            font-size: 12px;
            color: var(--text-secondary);
            margin-top: 8px;
        }

        .form-help a {
            color: var(--primary);
            text-decoration: none;
        }

        .toast {
            position: fixed;
            bottom: 100px;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background: var(--bg-dark);
            border: 1px solid rgba(99, 102, 241, 0.3);
            color: white;
            padding: 16px 28px;
            border-radius: 12px;
            font-size: 14px;
            font-weight: 600;
            z-index: 2000;
            opacity: 0;
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .toast.show {
            opacity: 1;
            transform: translateX(-50%) translateY(0);
        }

        .toast.success {
            border-color: var(--success);
            background: rgba(16, 185, 129, 0.1);
        }

        .toast.error {
            border-color: var(--error);
            background: rgba(239, 68, 68, 0.1);
        }

        .toast.warning {
            border-color: var(--warning);
            background: rgba(245, 158, 11, 0.1);
        }

        .spinner {
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-top-color: white;
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .history-item {
            background: #000000;
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .history-item:hover {
            border-color: var(--primary);
            transform: translateX(5px);
        }

        .history-date {
            font-size: 11px;
            color: var(--text-secondary);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .history-prompt {
            color: var(--text-primary);
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 10px;
        }

        .history-files {
            font-size: 11px;
            color: var(--success);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .empty-history {
            text-align: center;
            padding: 60px 20px;
            color: var(--text-secondary);
        }

        .empty-history i {
            font-size: 48px;
            margin-bottom: 20px;
            opacity: 0.3;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 16px;
            }

            .workspace {
                padding: 25px;
            }

            .input-section {
                padding: 20px;
            }

            .nav-buttons {
                gap: 8px;
            }

            .nav-btn {
                padding: 8px 16px;
                font-size: 12px;
            }

            .stats-bar {
                padding: 30px 20px;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn-primary, .btn-secondary {
                width: 100%;
                justify-content: center;
            }

            .editor {
                font-size: 13px;
            }

            .line-numbers {
                width: 40px;
                font-size: 13px;
            }

            .editor-wrapper {
                padding-left: 40px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 28px;
            }

            .workspace {
                padding: 20px;
            }

            .tab {
                padding: 10px 16px;
                font-size: 13px;
            }

            .action-btn {
                padding: 10px 16px;
                font-size: 13px;
            }

            .modal-content {
                padding: 25px;
            }
        }
    </style>
</head>
<body>
    <div class="grid-bg"></div>
    
    <div class="emoji-float emoji-1">🚀</div>
    <div class="emoji-float emoji-2">⚡</div>
    <div class="emoji-float emoji-3">💻</div>
    <div class="emoji-float emoji-4">🔧</div>
    <div class="emoji-float emoji-5">🎮</div>
    <div class="emoji-float emoji-6">📁</div>
    <div class="emoji-float emoji-7">⚙️</div>
    <div class="emoji-float emoji-8">🎯</div>

    <div class="container">
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-bolt"></i>
                NETHER AI
                <span class="logo-badge">PRO</span>
            </div>
            <div class="nav-buttons">
                <button class="nav-btn" onclick="openHistory()">
                    <i class="fas fa-history"></i>
                    History
                </button>
                <button class="nav-btn" onclick="openSettings()">
                    <i class="fas fa-cog"></i>
                    Settings
                </button>
                <button class="nav-btn" onclick="openTemplates()">
                    <i class="fas fa-magic"></i>
                    Templates
                </button>
            </div>
        </nav>

        <section class="hero">
            <div class="hero-badge">
                <i class="fas fa-sparkles"></i>
                THE SKY IS THE LIMIT
            </div>
            <h1>Revolutionizing Roblox Development</h1>
            <p>Generate professional Roblox/Luau code instantly with AI. Perfect for game systems, tools, and complete projects.</p>
            <div class="hero-buttons">
                <button class="btn-primary" onclick="scrollToWorkspace()">
                    <i class="fas fa-rocket"></i>
                    Start Creating
                </button>
                <button class="btn-secondary" onclick="openSettings()">
                    <i class="fas fa-gear"></i>
                    Configure API
                </button>
            </div>
        </section>

        <div class="stats-bar">
            <div class="stat-item">
                <div class="stat-value" id="statGenerations">0</div>
                <div class="stat-label">Generations</div>
            </div>
            <div class="stat-item">
                <div class="stat-value" id="statLines">0</div>
                <div class="stat-label">Lines of Code</div>
            </div>
            <div class="stat-item">
                <div class="stat-value" id="statFiles">0</div>
                <div class="stat-label">Files Created</div>
            </div>
            <div class="stat-item">
                <div class="stat-value" id="statTokens">0</div>
                <div class="stat-label">Tokens Used</div>
            </div>
        </div>

        <div class="workspace" id="workspace">
            <div class="workspace-header">
                <div class="workspace-title">
                    <i class="fas fa-code"></i>
                    Code Generator
                </div>
                <div class="workspace-status" id="workspaceStatus">
                    <i class="fas fa-circle"></i>
                    Ready
                </div>
            </div>

            <div class="tabs">
                <div class="tab active" onclick="switchTab('server')">
                    <i class="fas fa-server"></i>
                    Server.luau
                </div>
                <div class="tab" onclick="switchTab('client')">
                    <i class="fas fa-desktop"></i>
                    Client.luau
                </div>
                <div class="tab" onclick="switchTab('shared')">
                    <i class="fas fa-share-nodes"></i>
                    Shared.luau
                </div>
                <div class="tab" onclick="switchTab('manifest')">
                    <i class="fas fa-hammer"></i>
                    Setup Guide
                </div>
                <div class="tab" onclick="switchTab('blender')">
                    <i class="fab fa-blender"></i>
                    Blender.py
                </div>
            </div>

            <div class="editor-container">
                <div class="line-numbers" id="lineNumbers">1</div>
                <div class="editor-wrapper">
                    <div class="editor" id="editor" contenteditable="false">-- Welcome to Nether AI Code Generator
-- Describe what you want to build in the input below
-- Then click the generate button to create your code

-- Example: "Create a combat system with health, damage, and special abilities"
-- Example: "Make a shop system with in-game currency and item purchases"
-- Example: "Build a leaderboard system with player rankings and rewards"

-- Click on different tabs to view generated code for each section
-- Use the buttons below to copy, download, or share your code</div>
                </div>
                <div class="editor-info">
                    <div id="fileInfo">server.luau</div>
                    <div id="codeInfo">0 lines | 0 characters</div>
                </div>
            </div>

            <div class="editor-actions">
                <button class="action-btn action-btn-primary" onclick="copyCode()">
                    <i class="fas fa-copy"></i>
                    Copy Code
                </button>
                <button class="action-btn" onclick="downloadCode()">
                    <i class="fas fa-download"></i>
                    Download
                </button>
                <button class="action-btn" onclick="exportAll()">
                    <i class="fas fa-file-export"></i>
                    Export All
                </button>
                <button class="action-btn" onclick="clearWorkspace()">
                    <i class="fas fa-trash"></i>
                    Clear
                </button>
            </div>
        </div>

        <div class="input-section">
            <div class="input-wrapper">
                <textarea 
                    class="input-field" 
                    id="promptInput" 
                    placeholder="Describe your Roblox system... (e.g., 'Create a combat system with combo attacks and special moves')"
                    onkeydown="handleKeyPress(event)"
                ></textarea>
                <button class="send-btn" id="generateBtn" onclick="generate()">
                    <i class="fas fa-paper-plane"></i>
                </button>
            </div>
            
            <div class="templates">
                <button class="template-btn" onclick="useTemplate('combat')">
                    ⚔️ Combat System
                </button>
                <button class="template-btn" onclick="useTemplate('shop')">
                    🛒 Shop System
                </button>
                <button class="template-btn" onclick="useTemplate('leaderboard')">
                    🏆 Leaderboard
                </button>
                <button class="template-btn" onclick="useTemplate('inventory')">
                    🎒 Inventory
                </button>
                <button class="template-btn" onclick="useTemplate('vehicle')">
                    🚗 Vehicle System
                </button>
                <button class="template-btn" onclick="useTemplate('quest')">
                    📜 Quest System
                </button>
                <button class="template-btn" onclick="useTemplate('chat')">
                    💬 Chat System
                </button>
                <button class="template-btn" onclick="useTemplate('settings')">
                    ⚙️ Settings Menu
                </button>
            </div>
        </div>
    </div>

    <div class="modal" id="settingsModal">
        <div class="modal-content">
            <div class="modal-header">
                <span><i class="fas fa-cog"></i> Settings</span>
                <span class="modal-close" onclick="closeSettings()">&times;</span>
            </div>

            <div class="form-group">
                <label class="form-label">DeepSeek API Key</label>
                <input 
                    type="password" 
                    class="form-input" 
                    id="apiKeyInput"
                    placeholder="sk-xxxxxxxxxxxxxxxx"
                >
                <div class="form-help">
                    Get your free API key from <a href="https://platform.deepseek.com" target="_blank">platform.deepseek.com</a>
                </div>
            </div>

            <div class="form-group">
                <label class="form-label">AI Model</label>
                <select class="form-input" id="modelSelect">
                    <option value="deepseek-reasoner">DeepSeek Reasoner (Best Quality)</option>
                    <option value="deepseek-chat">DeepSeek Chat (Faster)</option>
                </select>
            </div>

            <div class="form-group">
                <label class="form-label">Code Style</label>
                <select class="form-input" id="styleSelect">
                    <option value="professional">Professional (Production Ready)</option>
                    <option value="commented">Well Commented (Easy to Read)</option>
                    <option value="beginner">Beginner Friendly (Educational)</option>
                </select>
            </div>

            <div class="editor-actions">
                <button class="action-btn action-btn-primary" onclick="saveSettings()">
                    <i class="fas fa-save"></i>
                    Save Settings
                </button>
                <button class="action-btn" onclick="closeSettings()">
                    Cancel
                </button>
            </div>
        </div>
    </div>

    <div class="modal" id="historyModal">
        <div class="modal-content" style="max-width: 800px;">
            <div class="modal-header">
                <span><i class="fas fa-history"></i> Generation History</span>
                <span class="modal-close" onclick="closeHistory()">&times;</span>
            </div>

            <div id="historyList" style="max-height: 500px; overflow-y: auto;"></div>

            <div class="editor-actions">
                <button class="action-btn" style="background: rgba(239, 68, 68, 0.1); border-color: var(--error);" onclick="clearHistory()">
                    <i class="fas fa-trash"></i>
                    Clear All History
                </button>
                <button class="action-btn" onclick="closeHistory()">
                    Close
                </button>
            </div>
        </div>
    </div>

    <div class="modal" id="templatesModal">
        <div class="modal-content" style="max-width: 700px;">
            <div class="modal-header">
                <span><i class="fas fa-magic"></i> Quick Templates</span>
                <span class="modal-close" onclick="closeTemplates()">&times;</span>
            </div>

            <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 15px; margin-bottom: 30px;">
                <div class="template-card" onclick="loadTemplate('combat')">
                    <div style="font-size: 24px; margin-bottom: 10px;">⚔️</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Combat System</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Health, damage, abilities, hit detection</div>
                </div>
                <div class="template-card" onclick="loadTemplate('shop')">
                    <div style="font-size: 24px; margin-bottom: 10px;">🛒</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Shop System</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Currency, purchases, inventory management</div>
                </div>
                <div class="template-card" onclick="loadTemplate('leaderboard')">
                    <div style="font-size: 24px; margin-bottom: 10px;">🏆</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Leaderboard</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Player rankings, rewards, stats tracking</div>
                </div>
                <div class="template-card" onclick="loadTemplate('inventory')">
                    <div style="font-size: 24px; margin-bottom: 10px;">🎒</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Inventory</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Item storage, equipment, weight system</div>
                </div>
                <div class="template-card" onclick="loadTemplate('vehicle')">
                    <div style="font-size: 24px; margin-bottom: 10px;">🚗</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Vehicle System</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Driving physics, fuel, damage, controls</div>
                </div>
                <div class="template-card" onclick="loadTemplate('quest')">
                    <div style="font-size: 24px; margin-bottom: 10px;">📜</div>
                    <div style="font-weight: 600; margin-bottom: 5px;">Quest System</div>
                    <div style="font-size: 12px; color: var(--text-secondary);">Missions, objectives, rewards, progress</div>
                </div>
            </div>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <script>
        let config = {
            apiKey: localStorage.getItem('netherApiKey') || '',
            model: localStorage.getItem('netherModel') || 'deepseek-reasoner',
            style: localStorage.getItem('netherStyle') || 'professional'
        };

        let session = {
            server: '',
            client: '',
            shared: '',
            manifest: '',
            blender: '',
            currentTab: 'server',
            history: JSON.parse(localStorage.getItem('netherHistory') || '[]')
        };

        let stats = {
            generations: parseInt(localStorage.getItem('netherGenerations') || '0'),
            lines: 0,
            files: 0,
            tokens: parseInt(localStorage.getItem('netherTokens') || '0')
        };

        const templates = {
            combat: "Create a complete combat system for a Roblox game including: health system, damage calculation, hit detection, special abilities with cooldowns, combo system, and visual effects for hits. Make it modular and easy to extend.",
            shop: "Build a shop system for a Roblox game with: in-game currency, item purchases, inventory management, limited-time offers, and a clean GUI. Include both server-side validation and client-side interface.",
            leaderboard: "Create a leaderboard system that tracks player stats (kills, deaths, wins), displays rankings, gives rewards based on position, and updates in real-time. Include weekly/monthly resets.",
            inventory: "Design an inventory system with: item slots, equipment management, item stacking, weight limits, drag-and-drop interface, and item descriptions.",
            vehicle: "Create a vehicle system with: driving physics, fuel management, damage system, different vehicle types (car, plane, boat), and player controls.",
            quest: "Build a quest/mission system with: multiple quest types (collect, kill, deliver), objective tracking, rewards, quest log UI, and NPC interaction.",
            chat: "Create a custom chat system with: chat commands (/me, /whisper), chat bubbles, profanity filter, admin commands, and chat history.",
            settings: "Design a settings menu with: graphics options, audio controls, keybind customization, and save/load functionality."
        };

        window.onload = function() {
            loadSession();
            updateStats();
            updateLineNumbers();
            checkApiKey();
            updateCodeInfo();
            setupKeyboardShortcuts();
        };

        function loadSession() {
            const saved = localStorage.getItem('netherSession');
            if (saved) {
                try {
                    const data = JSON.parse(saved);
                    session.server = data.server || '';
                    session.client = data.client || '';
                    session.shared = data.shared || '';
                    session.manifest = data.manifest || '';
                    session.blender = data.blender || '';
                    session.currentTab = data.currentTab || 'server';
                    
                    switchTab(session.currentTab);
                } catch (e) {
                    console.error('Failed to load session:', e);
                }
            }
        }

        function saveSession() {
            localStorage.setItem('netherSession', JSON.stringify(session));
        }

        function checkApiKey() {
            const status = document.getElementById('workspaceStatus');
            if (!config.apiKey) {
                status.innerHTML = '<i class="fas fa-circle"></i> API Key Required';
                status.classList.add('error');
                showToast('⚠️ Please configure your API key in Settings', 'warning');
            } else {
                status.innerHTML = '<i class="fas fa-circle"></i> Ready';
                status.classList.remove('error');
            }
        }

        function scrollToWorkspace() {
            document.getElementById('workspace').scrollIntoView({ behavior: 'smooth' });
            document.getElementById('promptInput').focus();
        }

        async function generate() {
            const prompt = document.getElementById('promptInput').value.trim();
            
            if (!prompt) {
                showToast('❌ Please enter a description', 'error');
                return;
            }

            if (!config.apiKey) {
                showToast('❌ API key not configured!', 'error');
                openSettings();
                return;
            }

            const btn = document.getElementById('generateBtn');
            btn.disabled = true;
            btn.innerHTML = '<div class="spinner"></div>';

            const status = document.getElementById('workspaceStatus');
            status.innerHTML = '<i class="fas fa-circle"></i> Generating...';

            document.getElementById('editor').textContent = '-- Connecting to DeepSeek API...\n-- Generating code...\n-- Please wait...';
            updateLineNumbers();
            updateCodeInfo();

            try {
                const systemPrompt = getSystemPrompt();

                const response = await fetch('https://api.deepseek.com/chat/completions', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                        'Authorization': `Bearer ${config.apiKey}`,
                        'Accept': 'application/json'
                    },
                    body: JSON.stringify({
                        model: config.model,
                        messages: [
                            { role: 'system', content: systemPrompt },
                            { role: 'user', content: prompt }
                        ],
                        temperature: 0.7,
                        max_tokens: 4000,
                        stream: false
                    })
                });

                if (!response.ok) {
                    const errorData = await response.json().catch(() => ({}));
                    throw new Error(errorData.error?.message || `HTTP Error ${response.status}: ${response.statusText}`);
                }

                const data = await response.json();
                const content = data.choices[0].message.content;

                session.server = extractSection(content, 'SERVER') || '-- Server code will be generated here';
                session.client = extractSection(content, 'CLIENT') || '-- Client code will be generated here';
                session.shared = extractSection(content, 'SHARED') || '-- Shared modules will be generated here';
                session.manifest = extractSection(content, 'MANIFEST') || '-- Setup instructions will be generated here';
                session.blender = extractSection(content, 'BLENDER') || '# Blender script will be generated here';

                switchTab(session.currentTab);

                stats.generations++;
                stats.files = countFiles();
                stats.tokens += data.usage?.total_tokens || 0;
                stats.lines = session[session.currentTab].split('\n').length;
                
                localStorage.setItem('netherGenerations', stats.generations);
                localStorage.setItem('netherTokens', stats.tokens);
                updateStats();

                saveToHistory(prompt, content);
                saveSession();

                showToast('✅ Generation complete! Code ready.', 'success');
                status.innerHTML = '<i class="fas fa-circle"></i> Ready';
                document.getElementById('promptInput').value = '';

            } catch (error) {
                console.error('Generation error:', error);
                
                let errorMessage = error.message;
                if (error.message.includes('401')) errorMessage = 'Invalid API key. Please check Settings.';
                else if (error.message.includes('429')) errorMessage = 'Rate limit exceeded. Please wait.';
                else if (error.message.includes('network')) errorMessage = 'Network error. Check your connection.';
                
                document.getElementById('editor').textContent = `-- Generation failed\n-- Error: ${errorMessage}\n\n-- Check your API key and internet connection\n-- Then try again`;
                
                showToast(`❌ ${errorMessage}`, 'error');
                status.innerHTML = '<i class="fas fa-circle"></i> Error';
                status.classList.add('error');
                
                updateLineNumbers();
                updateCodeInfo();
            } finally {
                btn.disabled = false;
                btn.innerHTML = '<i class="fas fa-paper-plane"></i>';
            }
        }

        function getSystemPrompt() {
            const styles = {
                professional: 'Write clean, production-ready code following Roblox best practices. Use efficient patterns, proper error handling, and minimal comments.',
                commented: 'Write well-commented code explaining each major function and section. Include explanations for complex logic.',
                beginner: 'Write educational code with detailed comments explaining each step. Use simple patterns and explain concepts.'
            };

            return `You are Nether AI, an expert Roblox/Luau code generator.

IMPORTANT: Format your response with these exact section headers:
[SERVER] - ServerScriptService scripts
[CLIENT] - StarterPlayer scripts and GUIs
[SHARED] - ReplicatedStorage modules and utilities
[MANIFEST] - Setup instructions for Roblox Studio
[BLENDER] - Python scripts for 3D assets (if applicable)

${styles[config.style]}

Requirements:
1. Generate complete, working code
2. Use modern Luau features
3. Include proper error handling
4. Optimize for performance
5. Follow Roblox security practices

Start each section immediately after the header.`;
        }

        function extractSection(text, tag) {
            const regex = new RegExp(`\\[${tag}\\]([\\s\\S]*?)(?=\\[[A-Z]+\\]|$)`, 'i');
            const match = text.match(regex);
            return match ? match[1].trim() : '';
        }

        function switchTab(tabName) {
            session.currentTab = tabName;
            
            document.querySelectorAll('.tab').forEach(tab => tab.classList.remove('active'));
            const activeTab = Array.from(document.querySelectorAll('.tab')).find(tab => 
                tab.textContent.toLowerCase().includes(tabName)
            );
            if (activeTab) activeTab.classList.add('active');

            const code = session[tabName] || getDefaultContent(tabName);
            const editor = document.getElementById('editor');
            if (tabName === 'blender' || tabName === 'manifest') {
                editor.textContent = code;
            } else {
                editor.innerHTML = highlightCode(code);
            }

            const fileInfo = document.getElementById('fileInfo');
            const fileNames = {
                server: 'server.luau',
                client: 'client.luau',
                shared: 'shared.luau',
                manifest: 'setup_guide.txt',
                blender: 'blender_script.py'
            };
            fileInfo.textContent = fileNames[tabName];

            stats.lines = code.split('\n').length;
            updateStats();
            updateLineNumbers();
            updateCodeInfo();
        }

        function getDefaultContent(tabName) {
            const defaults = {
                server: '-- Server-side code will appear here\n-- Click generate to create your system',
                client: '-- Client-side code will appear here\n-- This includes GUIs and local scripts',
                shared: '-- Shared modules will appear here\n-- Place shared constants and utilities here',
                manifest: '-- Setup instructions will appear here\n-- Follow these steps to implement in Roblox Studio',
                blender: '# Blender Python scripts will appear here\n# Use these for 3D modeling automation'
            };
            return defaults[tabName] || '-- Content will appear here';
        }

        function highlightCode(code) {
            return code
                .replace(/--(.*)$/gm, '<span class="cmt">--$1</span>')
                .replace(/\b(local|function|end|if|then|else|elseif|return|for|while|do|repeat|until|break|continue|in|and|or|not)\b/g, '<span class="kw">$1</span>')
                .replace(/\b(game|workspace|task|wait|spawn|delay|print|warn|error|pcall|GetService|WaitForChild|FindFirstChild)\b/g, '<span class="fn">$1</span>')
                .replace(/\b(Vector3|CFrame|UDim2|UDim|Color3|NumberRange|Random|math|table|string)\b/g, '<span class="var">$1</span>')
                .replace(/"([^"]*)"/g, '<span class="str">"$1"</span>')
                .replace(/'([^']*)'/g, '<span class="str">\'$1\'</span>')
                .replace(/\b(\d+\.?\d*)\b/g, '<span class="num">$1</span>');
        }

        function updateLineNumbers() {
            const code = session[session.currentTab] || '';
            const lines = code.split('\n').length || 1;
            let numbers = '';
            
            for (let i = 1; i <= lines; i++) {
                numbers += i + '<br>';
            }
            
            document.getElementById('lineNumbers').innerHTML = numbers;
        }

        function updateCodeInfo() {
            const code = session[session.currentTab] || '';
            const lines = code.split('\n').length;
            const chars = code.length;
            document.getElementById('codeInfo').textContent = `${lines} lines | ${chars.toLocaleString()} characters`;
        }

        function countFiles() {
            let count = 0;
            ['server', 'client', 'shared', 'manifest', 'blender'].forEach(type => {
                const content = session[type];
                if (content && content.length > 50 && !content.includes('will be generated')) {
                    count++;
                }
            });
            return count;
        }

        function updateStats() {
            document.getElementById('statGenerations').textContent = stats.generations.toLocaleString();
            document.getElementById('statLines').textContent = stats.lines.toLocaleString();
            document.getElementById('statFiles').textContent = stats.files;
            document.getElementById('statTokens').textContent = stats.tokens.toLocaleString();
        }

        function copyCode() {
            const code = session[session.currentTab];
            if (!code || code.includes('will be generated')) {
                showToast('❌ No code to copy! Generate some first.', 'error');
                return;
            }

            navigator.clipboard.writeText(code).then(() => {
                showToast('✅ Code copied to clipboard!', 'success');
            }).catch(err => {
                showToast('❌ Failed to copy: ' + err.message, 'error');
            });
        }

        function downloadCode() {
            const code = session[session.currentTab];
            if (!code || code.includes('will be generated')) {
                showToast('❌ No code to download!', 'error');
                return;
            }

            const extensions = {
                server: '.luau',
                client: '.luau',
                shared: '.luau',
                manifest: '.txt',
                blender: '.py'
            };

            const filename = `${session.currentTab}${extensions[session.currentTab] || '.txt'}`;
            const blob = new Blob([code], { type: 'text/plain' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = filename;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);

            showToast(`✅ Downloaded ${filename}`, 'success');
        }

        function exportAll() {
            const files = [
                { name: 'server.luau', content: session.server },
                { name: 'client.luau', content: session.client },
                { name: 'shared.luau', content: session.shared },
                { name: 'setup_guide.txt', content: session.manifest },
                { name: 'blender_script.py', content: session.blender }
            ];

            let hasContent = false;
            files.forEach(file => {
                if (file.content && file.content.length > 50 && !file.content.includes('will be generated')) {
                    hasContent = true;
                }
            });

            if (!hasContent) {
                showToast('❌ No generated content to export!', 'error');
                return;
            }

            const zipContent = files.map(file => 
                `=== ${file.name} ===\n${file.content}\n\n`
            ).join('');

            const blob = new Blob([zipContent], { type: 'text/plain' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'nether_ai_project.txt';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);

            showToast('✅ Exported all files!', 'success');
        }

        function clearWorkspace() {
            if (confirm('Clear all generated code? This cannot be undone.')) {
                session.server = '';
                session.client = '';
                session.shared = '';
                session.manifest = '';
                session.blender = '';
                session.currentTab = 'server';
                
                switchTab('server');
                saveSession();
                
                showToast('✅ Workspace cleared', 'success');
            }
        }

        function openSettings() {
            document.getElementById('settingsModal').classList.add('show');
            document.getElementById('apiKeyInput').value = config.apiKey;
            document.getElementById('modelSelect').value = config.model;
            document.getElementById('styleSelect').value = config.style;
        }

        function closeSettings() {
            document.getElementById('settingsModal').classList.remove('show');
        }

        function saveSettings() {
            config.apiKey = document.getElementById('apiKeyInput').value.trim();
            config.model = document.getElementById('modelSelect').value;
            config.style = document.getElementById('styleSelect').value;

            localStorage.setItem('netherApiKey', config.apiKey);
            localStorage.setItem('netherModel', config.model);
            localStorage.setItem('netherStyle', config.style);

            showToast('✅ Settings saved!', 'success');
            closeSettings();
            checkApiKey();
        }

        function openHistory() {
            document.getElementById('historyModal').classList.add('show');
            displayHistory();
        }

        function closeHistory() {
            document.getElementById('historyModal').classList.remove('show');
        }

        function openTemplates() {
            document.getElementById('templatesModal').classList.add('show');
        }

        function closeTemplates() {
            document.getElementById('templatesModal').classList.remove('show');
        }

        function saveToHistory(prompt, response) {
            const entry = {
                id: Date.now(),
                timestamp: new Date().toISOString(),
                prompt: prompt,
                preview: prompt.substring(0, 100) + (prompt.length > 100 ? '...' : ''),
                files: countFiles(),
                response: response
            };

            session.history.unshift(entry);
            session.history = session.history.slice(0, 50);
            localStorage.setItem('netherHistory', JSON.stringify(session.history));
        }

        function displayHistory() {
            const historyList = document.getElementById('historyList');
            
            if (session.history.length === 0) {
                historyList.innerHTML = `
                    <div class="empty-history">
                        <i class="fas fa-inbox"></i>
                        <div>No generation history yet.</div>
                        <div style="font-size: 12px; margin-top: 10px;">Generate some code to see it here!</div>
                    </div>
                `;
                return;
            }

            historyList.innerHTML = session.history.map(entry => {
                const date = new Date(entry.timestamp);
                const timeStr = date.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
                const dateStr = date.toLocaleDateString();
                
                return `
                    <div class="history-item" onclick="loadHistoryEntry(${entry.id})">
                        <div class="history-date">
                            <i class="fas fa-clock"></i> ${dateStr} ${timeStr}
                        </div>
                        <div class="history-prompt">
                            ${entry.preview}
                        </div>
                        <div class="history-files">
                            <i class="fas fa-file-code"></i> ${entry.files} files generated
                        </div>
                    </div>
                `;
            }).join('');
        }

        function loadHistoryEntry(id) {
            const entry = session.history.find(item => item.id === id);
            if (!entry) return;

            const content = entry.response;
            session.server = extractSection(content, 'SERVER') || '';
            session.client = extractSection(content, 'CLIENT') || '';
            session.shared = extractSection(content, 'SHARED') || '';
            session.manifest = extractSection(content, 'MANIFEST') || '';
            session.blender = extractSection(content, 'BLENDER') || '';

            switchTab(session.currentTab);
            document.getElementById('promptInput').value = entry.prompt;
            
            closeHistory();
            scrollToWorkspace();
            showToast('✅ Loaded from history', 'success');
        }

        function clearHistory() {
            if (confirm('Clear all generation history? This cannot be undone.')) {
                session.history = [];
                localStorage.setItem('netherHistory', '[]');
                displayHistory();
                showToast('✅ History cleared', 'success');
            }
        }

        function useTemplate(templateName) {
            if (templates[templateName]) {
                document.getElementById('promptInput').value = templates[templateName];
                showToast(`✅ Loaded ${templateName} template`, 'success');
                scrollToWorkspace();
            }
        }

        function loadTemplate(templateName) {
            useTemplate(templateName);
            closeTemplates();
        }

        function showToast(message, type = 'success') {
            const toast = document.getElementById('toast');
            toast.innerHTML = message;
            toast.className = `toast ${type} show`;

            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        function handleKeyPress(event) {
            if (event.key === 'Enter' && (event.ctrlKey || event.metaKey)) {
                event.preventDefault();
                generate();
            }
        }

        function setupKeyboardShortcuts() {
            document.addEventListener('keydown', (e) => {
                if ((e.ctrlKey || e.metaKey) && e.key === 's') {
                    e.preventDefault();
                    if (document.getElementById('settingsModal').classList.contains('show')) {
                        saveSettings();
                    }
                }
                if ((e.ctrlKey || e.metaKey) && e.key === 'h') {
                    e.preventDefault();
                    openHistory();
                }
                if ((e.ctrlKey || e.metaKey) && e.key === 't') {
                    e.preventDefault();
                    openTemplates();
                }
                if (e.key === 'Escape') {
                    closeSettings();
                    closeHistory();
                    closeTemplates();
                }
            });
        }

        const textarea = document.getElementById('promptInput');
        textarea.addEventListener('input', function() {
            this.style.height = 'auto';
            this.style.height = Math.min(this.scrollHeight, 150) + 'px';
        });

        const style = document.createElement('style');
        style.textContent = `
            .template-card {
                background: rgba(99, 102, 241, 0.05);
                border: 1px solid rgba(99, 102, 241, 0.2);
                border-radius: 12px;
                padding: 20px;
                cursor: pointer;
                transition: all 0.3s ease;
                text-align: center;
            }
            .template-card:hover {
                border-color: var(--primary);
                background: rgba(99, 102, 241, 0.1);
                transform: translateY(-2px);
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
