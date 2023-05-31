<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <title>Rec Vida</title>

        <!-- Styles -->
        <style>
            body {
                font-family: 'Nunito', sans-serif;
                background-image: url('https://cdn.discordapp.com/attachments/977561366342823959/1103425347560689745/Imagem_do_WhatsApp_de_2023-05-03_as_17.15.55.jpg');
                background-size: cover;
                background-position: center;
            }

            .container {
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                height: 100vh;
            }

            .title {
                font-size: 3rem;
                font-weight: bold;
                text-align: center;
                margin-bottom: 1rem;
                color: #fff;
                text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            }

            .links {
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
            }

            .links a {
                margin: 0.5rem;
                padding: 1rem 2rem;
                border: 2px solid #fff;
                border-radius: 5px;
                text-decoration: none;
                font-size: 1.5rem;
                font-weight: bold;
                text-align: center;
                color: #fff;
                transition: all 0.3s ease-in-out;
            }

            .links a:hover {
                background-color: #fff;
                color: #000;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <h1 class="title">Rec Vida</h1>

            <div class="links">
    @if (Route::has('login'))
        @auth
            <a href="{{ url('/dashboard') }}">Dashboard</a>
        @else
            <a href="{{ route('login') }}">Entrar</a>

            @if (Route::has('register'))
                <a href="{{ route('register') }}">Criar conta</a>
            @endif

            <a href="https://recvida.my.canva.site" target="_blank">Conheça nossos serviços</a>
        @endauth
    @endif
</div>

        </div>
    </body>
</html>
