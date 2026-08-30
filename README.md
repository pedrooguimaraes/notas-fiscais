<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Painel Inicial - Home</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #f7f7f7;
            margin: 0;
            padding: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            box-sizing: border-box;
        }
        .dashboard-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            border: 1px solid #e0e0e0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            text-align: center;
            max-width: 400px;
            width: 100%;
        }
        h1 {
            font-size: 1.4rem;
            color: #333;
            margin-bottom: 10px;
        }
        p {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 25px;
        }
        .menu-buttons {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .btn-nav {
            padding: 12px 20px;
            border-radius: 6px;
            border: 1px solid #ccc;
            background-color: #fff;
            color: #333;
            text-decoration: none;
            font-weight: bold;
            font-size: 14px;
            transition: all 0.2s;
            display: inline-block;
        }
        .btn-nav:hover {
            background-color: #f0f0f0;
            border-color: #b0b0b0;
        }
        .btn-primary {
            background-color: #215598;
            color: white;
            border: none;
        }
        .btn-primary:hover {
            background-color: #194277;
        }
    </style>
</head>
<body>

    <div class="dashboard-card">
        <h1>Painel de Controle</h1>
        <p>Selecione a opção desejada abaixo:</p>
        
        <div class="menu-buttons">
            <a href="index.html" class="btn-nav">🏠 Home (Início)</a>
            
            <a href="notas.html" target="_blank" class="btn-nav btn-primary">📋 Página de Notas Fiscais</a>
        </div>
    </div>

</body>
</html>
