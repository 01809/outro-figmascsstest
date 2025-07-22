<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Slider</title>
  <style>
    :root {
      --shadowcolor: #6e0808;
    }

    body {
      background: linear-gradient(to left, #cac3c3f1, #b6b0b06c, #a8a2a23f);
    }

    header {
      margin-top: -10px;
      margin-left: -10px;
      width: 120%;
      height: 66px;
      background-image: linear-gradient(to right, #200101, var(--shadowcolor));
      box-shadow: 1px 2px 90px;
    }

    .checkidea-testprodu {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 30px;
    }

    .radios {
      display: flex;
      gap: 20px;
      margin-bottom: 20px;
      margin-left: 60px;
      margin-top: 40px;
    }

    input[type="radio"] {
      display: none;
    }

    .radios label {
      border: 1px solid var(--shadowcolor);
      height: 10px;
      width: 10px;
      border-radius: 20%;
    }

    .radioback {
      width: 20px;
      height: 20px;
      background-color: gray;
      border-radius: 50%;
      display: inline-block;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .hover-fliptest {
      position: relative;
      width: 280px;
      height: 390px;
      margin-bottom: 40px;
      border: 10px solid var(--shadowcolor);
      border-top-left-radius: 30px;
      border-bottom-right-radius: 20px;
      filter: blur(2px);
      transition: all 0.5s ease;
      perspective: 1000px;
    }

    input#iradio1:checked ~ .checkidea-testprodu #ilefter,
    input#iradio2:checked ~ .checkidea-testprodu #icenter,
    input#iradio3:checked ~ .checkidea-testprodu #irighter {
      filter: none;
      z-index: 2;
    }

    .flip {
      width: 100%;
      height: 100%;
      perspective: 1000px;
    }

    .flip-inner {
      width: 100%;
      height: 100%;
      position: relative;
      transition: transform 0.6s;
      transform-style: preserve-3d;
    }

    .hover-fliptest:hover .flip-inner {
      transform: rotateY(180deg);
    }

    .flip-front, .flip-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
    }

    .flip-back {
      transform: rotateY(180deg);
    }

    .flip-front img, .flip-back img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: inherit;
    }

    .slide-text {
      text-align: center;
      margin-top: 10px;
      color: #333;
      font-weight: 600;
    }

    footer {
      background-color: black;
      padding: 40px;
      margin-top: 12%;
      height: 110px;
      width: 120%;
    }

    .footer-textcontent {
      border-left: 2px solid;
      padding-left: 10px;
      margin-right: 82%;
      margin-top: 50px;
      margin-left: 210px;
      color: white;
      letter-spacing: 4px;
    }
  </style>
</head>
<body>
  <header></header>

  <input type="radio" id="iradio1" name="option" class="radioback">
  <input type="radio" id="iradio2" name="option" class="radioback" checked>
  <input type="radio" id="iradio3" class="radioback" name="option">

  <div class="checkidea-testprodu">
    <div class="hover-fliptest" id="ilefter">
      <div class="flip">
        <div class="flip-inner">
          <div class="flip-front">
            <img src="imagem1-frente.png">
          </div>
          <div class="flip-back">
            <img src="imagem1-verso.png">
          </div>
        </div>
      </div>
      <div class="slide-text">Texto 1</div>
    </div>

    <div class="hover-fliptest" id="icenter">
      <div class="flip">
        <div class="flip-inner">
          <div class="flip-front">
            <img src="imagem2-frente.png">
          </div>
          <div class="flip-back">
            <img src="imagem2-verso.png">
          </div>
        </div>
      </div>
      <div class="slide-text">Texto 2</div>
    </div>

    <div class="hover-fliptest" id="irighter">
      <div class="flip">
        <div class="flip-inner">
          <div class="flip-front">
            <img src="imagem3-frente.png">
          </div>
          <div class="flip-back">
            <img src="imagem3-verso.png">
          </div>
        </div>
      </div>
      <div class="slide-text">Texto 3</div>
    </div>
  </div>

  <div class="radios">
    <label for="iradio1"></label>
    <label for="iradio2"></label>
    <label for="iradio3"></label>
  </div>

  <footer>
    <div class="footer-textcontent">
      <p>&copy; 01809</p>
      <p>@andrey_damas</p>
    </div>
  </footer>
</body>
</html>
