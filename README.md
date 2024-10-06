<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no,initial-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>VPN</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200;500&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            font-weight: 200;
            color: var(--tg-theme-text-color);
            background: var(--tg-theme-bg-color);
        }

        #main {
            width: 100%;
            padding: 20px;
            text-align: center;
        }

        h1 {
            margin-top: 50px;
            margin-bottom: 10px;
        }

        img {
            width: 70px;
            margin: 30px auto;
        }

        p {
            width: 350px;
            margin: 0 auto;
        }

        button {
            border: 0;
            border-radius: 5px;
            margin-top: 50px;
            height: 60px;
            width: 200px;
            font-size: 20px;
            font-weight: 500;
            cursor: pointer;
            transition: all 500ms ease;
            color: var(--tg-theme-button-color);
            background: var (tg-theme-button-text-color);
        }

        button:hover {
            background: var(--tg-theme-secondary-bg-color);
        }
    </style>
</head>
<body>
    <div id="main">
        <h1>Vpn Service</h1>
        <img src="https://cdn-icons-png.flaticon.com/512/9915/9915587.png"
             <p>Быстро и легко подключись к впн и реши все свои проблемы.</p>
        <button id="free">Попробовать бесплатно</button>
        <button id="buy">Купить подписку</button>
    </div>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        let tg = window.Telegram.WebApp;
        let free = document.getElementById("free");
        let buy = document.getElementById("buy");
        let order = document.getElementById("order");
        tg.expand();

        buy.addEventListener("click", () => {
            document.getElementById("main").style.display = 'none'
            document.getElementById("form").style.display = 'block'
            document.getElementById("user_name").value = tg.initDataUnsafe.user.first_name
        })
    </script>

</body>
</html>
