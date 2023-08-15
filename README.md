<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido de Namoro</title>
    <style>
        body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-image: url('https://lh3.googleusercontent.com/pw/AIL4fc8DjvJcSEoOz8gSGLwOChFe2TcMoxnEv8bdwVxgRx-WiUQyaXt9OvHomK2UAped9qy7lvmrRp46_EAI3vZXY_zdEs48i7syN8yiYy82mTYLQmFgkm4fE6hRm0vXuFX7Dk4fPcgLYJ-SxFswH9VsTnSvSelztcZCTVkOEBFw2vSWFa0zDXMWhy5FeLv1uIRC-OCM_mJVbj97NeKZXWmDH4cpffEUeBe-1FcYU1W9YPD39B7jEXISFtmrPlM3xby9_YYKpBcFwdrOR5bEMC4Bq6Huxhb_vzzyKn5ijVYCVXV-9CVYl-SdWW4m-zh1mn5osxApTdd0qWVNMbl2czbRRHbGbBPBTAjGvimoizrqxXHhvmwd3bRPIK-WXBDFCsS3XitSyYH1ArSUqGK_Y_Oorbll3ZlHWOwvLeOvKqmFRALZW8fGsnb4AMCbpAzjLj8nqVYsjwADJri-EClPoZXkr2uOZtYDrzLphDBoPG1jBr4m5MIuI9FZbnMp_lx16_g1PFqoBSuvDwkK9eI0In6xrBSPNYGmjffxQCVptTJv9yx20ym4m6sIws0t1oe0RDHND3VkZoTFdqbCNMYaepfVIv_Vpm70_Lhyigsx7GNKT1qGaGrv22IgTONkaqr5NGMRlanztmOSW1rP--h65A2AUy5_fI1fT1JRGVR2T-spfDFY3dtgd6IJkGv20lXzA7nWI_3oCbDZKa0zNjc-MmYO_dkx7sJ7OMm1o1ez6yvOjk-LQevso_3bG3UfFPBUtNrQUQQd7e25hBs627Qi8jgAkLf7yHrZM_moyjue0R4mVBE6aQW8B0g1H6OnM6haXdIKiuQ6j6h7R9ycCIOzWkY0olZdx6lMGPSxHo9LE_HcVxQ6Mm8VHQhexnyjn_r0fYe09hkOYlCsyZPySxG6MGf74JJppf0=w465-h619-s-no?authuser=0');
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    font-family: Arial, sans-serif;
        }

        .container {
            text-align: center;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        }

        h1 {
            font-size: 36px;
            margin-bottom: 10px;
        }

        p {
            font-size: 18px;
            margin-bottom: 20px;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        .button-yes {
            background-color: #4CAF50;
            color: white;
        }

        .button-no {
            background-color: #FF5733;
            color: white;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #FFD700;
            opacity: 0.8;
            transform: rotate(45deg);
            animation: fall 4s ease-in-out infinite;
        }

        @keyframes fall {
            0% {
                transform: translateY(-100px) rotate(45deg);
            }
            100% {
                transform: translateY(calc(100vh + 100px)) rotate(45deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Pedido de Namoro</h1>
        <p>Eu gosto muito de você e quero criar um história com você ao meu lado. Você aceita namorar comigo?</p>
        <div class="buttons">
            <button class="button button-yes">Sim</button>
            <button class="button button-no">Não</button>
        </div>
    </div>
    <script>

const buttonYes = document.querySelector('.button-yes');
        buttonYes.addEventListener('click', () => {
            const confettiContainer = document.createElement('div');
            confettiContainer.classList.add('confetti-container');
            document.body.appendChild(confettiContainer);

            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti');
                confetti.style.left = Math.random() * window.innerWidth + 'px';
                confetti.style.animationDuration = Math.random() * 3 + 2 + 's';
                confetti.style.animationDelay = Math.random() * 2 + 's';
                confettiContainer.appendChild(confetti);
            }

            setTimeout(() => {
                confettiContainer.remove();
            }, 5000);

            window.alert("Agora você está namorando com Gabriel bonitão");
        });

        const buttonNo = document.querySelector('.button-no');
        buttonNo.addEventListener('click', () => {
            const maxX = window.innerWidth - buttonNo.clientWidth;
            const maxY = window.innerHeight - buttonNo.clientHeight;
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            buttonNo.style.position = 'absolute';
            buttonNo.style.left = randomX + 'px';
            buttonNo.style.top = randomY + 'px';
        });
    </script>
</body>
</html>
