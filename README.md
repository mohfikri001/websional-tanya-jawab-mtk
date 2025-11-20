# websional-tanya-jawab-mtk
<!doctype html>
<html lang="id">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MathPower - Eksponen Interaktif</title>
  <script src="/_sdk/data_sdk.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        html {
            height: 100%;
        }
        
        * {
            box-sizing: border-box;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes bounceSlow {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes scaleIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        @keyframes shine {
            0% { background-position: -200% center; }
            100% { background-position: 200% center; }
        }
        
        .animate-fade-in { animation: fadeIn 0.8s ease-out; }
        .animate-slide-down { animation: slideDown 0.6s ease-out; }
        .animate-slide-up { animation: slideUp 0.6s ease-out; }
        .animate-bounce-slow { animation: bounceSlow 2s ease-in-out infinite; }
        .animate-scale-in { animation: scaleIn 0.3s ease-out; }
        .animate-pulse { animation: pulse 2s ease-in-out infinite; }
        
        .shine-effect {
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            background-size: 200% 100%;
            animation: shine 3s infinite;
        }
        
        .tab-button {
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .tab-button::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .tab-button.active::before {
            transform: scaleX(1);
