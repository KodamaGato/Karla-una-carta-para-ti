# Karla-una-carta-para-ti
Un regalo especial 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Karla</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffeef2;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            text-align: center;
        }

        /* Contenedor de pétalos */
        .petals-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .petal {
            position: absolute;
            background-color: #ff4d6d;
            border-radius: 150% 0 150% 0;
            width: 15px;
            height: 15px;
            opacity: 0.8;
            animation: fall linear infinite;
        }

        @keyframes fall {
            0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
        }

        /* Corazón latiendo */
        .heart {
            position: relative;
            width: 100px;
            height: 90px;
            background-color: #e63946;
            margin: 0 auto 30px;
            transform: rotate(-45deg);
            animation: beat 0.8s infinite alternate;
            box-shadow: 0 0 40px rgba(230, 57, 70, 0.5);
        }

        .heart:before, .heart:after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: #e63946;
            border-radius: 50%;
        }

        .heart:before { top: -50px; left: 0; }
        .heart:after { left: 50px; top: 0; }

        @keyframes beat {
            to { transform: scale(1.2) rotate(-45deg); }
        }

        /* Contenido de la carta */
        .card {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            z-index: 10;
            max-width: 400px;
            border: 2px solid #ffb3c1;
        }

        h1 { color: #c9184a; font-size: 1.5rem; margin-bottom: 25px; }
        p { color: #590d22; font-weight: bold; margin-bottom: 20px; }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
        }

        button {
            padding: 10px 25px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: 0.3s;
        }

        #btn-si { background-color: #4fb560; color: white; }
        #btn-si:hover { background-color: #3d8f4b; transform: scale(1.1); }

        #btn-no { background-color: #ff4d6d; color: white; }

        .hidden { display: none; }
        
        .final-msg { color: #ff0054; font-size: 1.2rem;
        
