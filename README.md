<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cubo 3D</title>
    <style>
        /* Estilo geral */
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #111;
            perspective: 1000px; /* Profundidade para o 3D */
        }

        .cube {
            width: 200px;
            height: 200px;
            position: relative;
            transform-style: preserve-3d;
            animation: rotate 5s infinite linear;
        }

        /* Cada face do cubo */
        .face {
            position: absolute;
            width: 200px;
            height: 200px;
            background-color: rgba(255, 255, 255, 0.8);
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            color: #333;
        }

        /* Posições das faces */
        .front  { transform: translateZ(100px); }
        .back   { transform: rotateY(180deg) translateZ(100px); }
        .right  { transform: rotateY(90deg) translateZ(100px); }
        .left   { transform: rotateY(-90deg) translateZ(100px); }
        .top    { transform: rotateX(90deg) translateZ(100px); }
        .bottom { transform: rotateX(-90deg) translateZ(100px); }

        /* Animação de rotação */
        @keyframes rotate {
            from {
                transform: rotateX(0deg) rotateY(0deg);
            }
            to {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="cube">
        <div class="face front">Frente</div>
        <div class="face back">Trás</div>
        <div class="face right">Direita</div>
        <div class="face left">Esquerda</div>
        <div class="face top">Topo</div>
        <div class="face bottom">Base</div>
    </div>
</body>
</html>
  
