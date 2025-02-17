# Davidan
Magazin de haine
<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Magazinul Meu</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #f4f4f4; margin: 0; padding: 0; }
        h1 { background-color: #333; color: white; padding: 10px; }

        .reclama {
            width: 100%;
            background-color: yellow;
            padding: 10px;
            font-size: 20px;
            font-weight: bold;
            position: relative;
            white-space: nowrap;
            overflow: hidden;
            color: red;
        }

        .reclama span {
            position: absolute;
            animation: miscare 5s linear infinite;
        }

        @keyframes miscare {
            from { left: 100%; }
            to { left: -100%; }
        }

        .sold {
            font-size: 20px;
            font-weight: bold;
            margin: 20px;
            padding: 10px;
            background-color: white;
            display: inline-block;
            border: 2px solid black;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
        }

        .produs {
            border: 1px solid black;
            background-color: white;
            padding: 10px;
            margin: 10px;
            width: 200px;
            text-align: center;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        }

        .produs img {
            width: 100%;
            height: auto;
        }

        .produs button {
            background-color: green;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            width: 100%;
        }

        .produs button:hover { background-color: darkgreen; }
    </style>
</head>
<body>

    <h1>Bine ai venit la magazinul meu!</h1>

    <!-- Reclama animată -->
    <div class="reclama">
        <span>🔥 Reduceri de 50%! Comandă acum! 🔥</span>
    </div>

    <!-- Soldul utilizatorului -->
    <div class="sold">💰 Sold: <span id="sold">1600</span> lei</div>

    <!-- Produse -->
    <div class="container">
        <div class="produs">
            <h2>Produs 1</h2>
            <img src="produs1.jpg" alt="Produs 1">
            <p>Preț: 100 lei</p>
            <button onclick="cumpara(100)">Cumpără</button>
        </div>

        <div class="produs">
            <h2>Produs 2</h2>
            <img src="produs2.jpg" alt="Produs 2">
            <p>Preț: 200 lei</p>
            <button onclick="cumpara(200)">Cumpără</button>
        </div>

        <div class="produs">
            <h2>Produs 3</h2>
            <img src="produs3.jpg" alt="Produs 3">
            <p>Preț: 300 lei</p>
            <button onclick="cumpara(300)">Cumpără</button>
        </div>

        <div class="produs">
            <h2>Produs 4</h2>
            <img src="produs4.jpg" alt="Produs 4">
            <p>Preț: 400 lei</p>
            <button onclick="cumpara(400)">Cumpără</button>
        </div>
    </div>

    <!-- Script JavaScript pentru coșul de cumpărături -->
    <script>
        let sold = 1600;

        function cumpara(pret) {
            if (sold >= pret) {
                sold -= pret;
                document.getElementById("sold").innerText = sold;
                alert("Ai cumpărat produsul! Sold rămas: " + sold + " lei");
            } else {
                alert("Fonduri insuficiente! Ai doar " + sold + " lei.");
            }
        }
    </script>

</body>
</html>
