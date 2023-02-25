<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>experiment</title>

        <style>

            body {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                background-color: #FF6666;
                overflow: hidden;
                display: flex;
                align-items: center;
                justify-content: center;
                height: 50vh;
            }


            h1 {
                position: relative;
                color: #333;
                font-size: 3em;
                letter-spacing: 5px;
                border-bottom: 16px solid #333;
                line-height: 1.4;
                font-style: oblique;
                text-transform: uppercase;
            }

            h1::before {
                content: attr(data-text);
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                color: #330000;
                border-bottom: 16px solid #000033;
                animation: lod 2s linear infinite;
                overflow: hidden;
            }

            @keyframes lod {
                0% {
                    width: 0;
                }
                100% {
                    width: 100%;
                }
            }

            .button {
                position: absolute;
                top: 70%;
                left: 80%;
                transform: translate(-50%, -50%);
            }

            .button {
                font-size: 20px;
                font-weight: 700;
                color: #fff;
                text-decoration: none;
                font-family: sans-serif;
                background-color: #ffdc60;
                height: 60px;
                line-height: 60px;
                text-align: center;
                padding: 0 50px;
                z-index: 1;
                overflow: hidden;
                border-radius: 10px;
                text-transform: capitalize;
            }

            .button::after, .button::before {
                content:'';
                background-color: #57c9da;
                height: 50%;
                width: 0;
                position: absolute;
                transition: 0.3s cubic-bezier(
                    .785, .135, .15, .86
                    );
                -webkit-transition: 0.3s cubic-bezier(
                    785, .135, .15, .86
                    );
                z-index: -1;
            }

            .button:hover::before {
                width: 100%;
                right: 0;
                left: auto;
            }

            .button::before {
                top: 0;
                left: 0;
                right: auto;
            }

            .button:hover::after {
                width: 100%;
                left: 0;
                right: auto;
            }

            .button::after {
                bottom: 0;
                right: 0;
                left: auto;
            }

        </style>

    </head>
    <body>

        <h1 data-text="Loading...">
            Loading...
        </h1>

        <a href="https://www.facebook.com/hibari.sv" class="button">
            :)
        </a>

    </body>
</html>
