<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Caveat:wght@500&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;1,500&display=swap');

        :root {
            --mektup-renk: #651da8;
        }

        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f7a3f2;
            overflow: hidden;
            perspective: 1000px;

        }

        .zarf {
            position: absolute;
            width: 300px;
            height: 200px;
            transform-style: preserve-3d;
            transition: transform 0.5s ease 3s;
        }

        .üstüçgen {
            position: absolute;
            width: 0;
            height: 0;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-top: 150px solid transparent;
            z-index: 5;
            cursor: pointer;
        }

        .üstüçgen::before {
            content: "";
            position: absolute;
            width: 0;
            height: 0;
            top: -100px;
            left: -150px;

            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-top: 150px solid var(--mektup-renk);
            transform-style: preserve-3d;
            transition: transform 0.8s;
            transform-origin: top;
            cursor: pointer;
        }

        .altüçgen {
            position: absolute;
            width: 0;
            height: 0;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-bottom: 150px solid transparent;
            z-index: 4;
        }

        .altüçgen::before {
            content: "";
            position: absolute;
            width: 0;
            height: 0;
            top: 45px;
            left: -150px;
            border-left: 150px solid var(--mektup-renk);
            border-right: 150px solid var(--mektup-renk);
            border-top: 150px solid transparent;
            margin-top: 10px;
        }


        .altkisim {
            position: absolute;
            display: block;
            z-index: 7;
            width: 300px;
            height: 50px;
            background-color: var(--mektup-renk);
            margin-left: -150px;
            top: 200px;
        }

        .arkakisim {
            position: absolute;
            display: block;
            z-index: 1;
            width: 300px;
            height: 200px;
            background-color: #333;
            margin-top: 50px;
            box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.5);
        }

        .mektup-grubu {
            position: absolute;
            z-index: 3;
            width: 130px;
            height: 170px;
            margin-top: -20px;
            margin-left: 83px;
            transform-style: preserve-3d;
            transition: transform 0.7s ease 1.5s, z-index 0s ease 0.5s;
        }

        .kagit1 {
            position: absolute;
            display: inline-block;
            width: 130px;
            height: 170px;
            background-color: #fff;
            margin-top: 100px;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
        }

        .kagit2 {
            position: absolute;
            display: inline-block;
            width: 130px;
            height: 170px;
            background-color: #C25283;
            margin-top: 100px;
            transform-origin: left;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
            transition: transform 0.7s ease;
            transform-style: preserve-3d;
            cursor: pointer;
        }


        .onyuz {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
        }

        .arkayuz {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-top-left-radius: 5px;
            border-bottom-left-radius: 5px;
            background-color: aliceblue;
            transform: rotateY(180deg);
        }

        .defteryuvarlak1 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 18px;
            margin-left: 5px;
        }

        .defteryuvarlak2 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 38px;
            margin-left: 5px;
        }

        .defteryuvarlak3 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 58px;
            margin-left: 5px;
        }

        .defteryuvarlak4 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 78px;
            margin-left: 5px;
        }

        .defteryuvarlak5 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 98px;
            margin-left: 5px;
        }

        .defteryuvarlak6 {
            position: absolute;
            display: inline-block;
            background-color: #f7a3f2;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-top: 118px;
            margin-left: 5px;
        }

        .defterteli1 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 20px;
        }

        .defterteli2 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 40px;
        }

        .defterteli3 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 60px;
        }

        .defterteli4 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 80px;
        }

        .defterteli5 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 100px;
        }

        .defterteli6 {
            position: absolute;
            display: inline-block;
            background-color: #333;
            width: 10px;
            height: 5px;
            margin-top: 120px;
        }

        .baslik {
            position: absolute;
            width: 75px;
            height: 37px;
            border: 3px solid #333;
            border-radius: 3px;
            margin-top: 20px;
            margin-left: 38px;
            font-family: 'Great Vibes', cursive;
            font-size: 15px;
            line-height: 1.2;
            text-align: center;
            color: #850746;
        }

        .mesaj {
            font-family: 'Caveat', cursive;
            font-size: 7.6px;

            color: #333;
            text-align: center;
            line-height: 1.4;

            padding: 8px;
            margin: 0;
            box-sizing: border-box;
            width: 100%;
            height: 100%;

            overflow-y: auto;
        }

        .mesaj::-webkit-scrollbar {
            width: 2px;
        }

        .mesaj::-webkit-scrollbar-thumb {
            background-color: #C25283;
            border-radius: 5px;
        }

        .bubu {
            position: absolute;
            width: 80px;
            height: 80px;
            top: 37%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
        }

        .bubu img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        .yazi {
            position: absolute;
            font-size: 12px;
            top: 65%;
            left: 25%;
            font-family: 'Cormorant Garamond', serif;
            color: #5e472f;
        }

        #noBtn {
            position: absolute;
            width: 30px;
            height: 10px;
            top: 75%;
            left: 60%;
            font-size: 7px;
            background-color: #ff4757;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: top 0.3s, left 0.3s;
        }

        #yesbtn {
            position: absolute;
            width: 30px;
            height: 10px;
            top: 75%;
            left: 15%;
            font-size: 7px;
            background-color: #ff4757;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: top 0.3s, left 0.3s;
        }

        .üstüçgen.acik::before {
            transform: rotateX(180deg);
        }

        .üstüçgen.acik~.altüçgen {
            z-index: 7;
        }

        .üstüçgen.acik~.mektup-grubu {
            transform: translateY(-360px) scale(2);
            z-index: 6;
        }

        .üstüçgen.acik~.mektup-grubu.acil {

            transform: translate(120px, -120px) scale(1.6);
            transition: transform 0.7s ease;
        }

        .mektup-grubu.acil .kagit2 {
            transform: rotateY(-180deg);
        }

        .arkakisim,
        .üstüçgen,
        .altüçgen {

            transition: transform 0.8s ease 3s, opacity 0.8s ease 3s;
        }

        .zarf:has(.üstüçgen.acik) .üstüçgen,
        .zarf:has(.üstüçgen.acik) .arkakisim,
        .zarf:has(.üstüçgen.acik) .altüçgen {
            transform: scale(0.1);
            opacity: 0;
        }

        .ucusankalp {
            position: absolute;
            top: 60%;
            left: 37%;
            width: 20px;
            height: 20px;
            z-index: 10;
            --kalp-tonu: #ffdce8;
            background-color: var(--kalp-tonu);
            transform: rotate(-45deg);
            box-shadow: -2px 2px 5px rgba(0, 0, 0, 0.2);
            animation: kalpSuzulmesi 2s ease infinite;
        }

        .ucusankalp::before,
        .ucusankalp::after {
            content: "";
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: var(--kalp-tonu);
            border-radius: 50%;
        }

        .ucusankalp::before {
            top: -10px;
            left: 0;
        }

        .ucusankalp::after {
            top: 0;
            left: 10px;
        }


        @keyframes kalpSuzulmesi {

            0%,
            100% {


                transform: rotate(-45deg) translateX(0px) translateY(15px);
            }

            50% {

                transform: rotate(-45deg) translateX(15px) translateY(0px);
            }
        }

        #mutluSonEkran {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: rgba(247, 163, 242, 0.95);
            z-index: 9999;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            pointer-events: none;
            transition: opacity 1.5s ease;
        }

        #mutluSonEkran.goster {
            opacity: 1;
            pointer-events: auto;
        }

        .kocaman-kalp {
            width: 100px;
            height: 100px;
            background-color: #ff4757;
            transform: rotate(-45deg);
            position: relative;
            animation: kalpAtisi 1s infinite alternate;
            box-shadow: 0 0 50px rgba(255, 71, 87, 0.6);
        }

        .kocaman-kalp::before,
        .kocaman-kalp::after {
            content: "";
            width: 100px;
            height: 100px;
            background-color: #ff4757;
            border-radius: 50%;
            position: absolute;
        }

        .kocaman-kalp::before {
            top: -50px;
            left: 0;
        }

        .kocaman-kalp::after {
            top: 0;
            left: 50px;
        }


        @keyframes kalpAtisi {
            0% {
                transform: rotate(-45deg) scale(1);
            }

            100% {
                transform: rotate(-45deg) scale(1.2);
            }
        }

        .son-mesaj {
            font-family: 'Great Vibes', cursive;
            font-size: 45px;
            color: #850746;
            margin-top: 80px;
            text-align: center;
            line-height: 1.2;
            text-shadow: 2px 2px 5px rgba(255, 255, 255, 0.8);
        }
    </style>
</head>

<body>
    <div class="zarf">
        <div class="üstüçgen" onclick="this.classList.toggle('acik')"></div>
        <div class="altüçgen">
            <div class="altkisim"></div>
        </div>
        <div class="arkakisim"></div>
        <div class="mektup-grubu" onclick="this.classList.toggle('acil')">
            <div class="kagit1">
                <div class="bubu"><img src="cute-bear.gif" alt=""></div>
                <div class="yazi">Benimle Misin ?</div>
                <button id="yesbtn" onclick="evetTiklandi(event)">EVET</button>
                <button id="noBtn" onmouseover="kac(event)" onclick="kac(event)">HAYIR</button>

                <script>
                    function kac(e) {
                        e.stopPropagation();

                        var buton = document.getElementById("noBtn");

                        var rastgeleX = Math.floor(Math.random() * 90) + 10;
                        var rastgeleY = Math.floor(Math.random() * 110) + 10;

                        buton.style.left = rastgeleX + "px";
                        buton.style.top = rastgeleY + "px";
                    }

                    function evetTiklandi(e) {
                        e.stopPropagation();

                        document.getElementById("mutluSonEkran").classList.add("goster");
                    }
                </script>
            </div>
            <div class="kagit2">
                <div class="onyuz">
                    <div class="defteryuvarlak1"></div>
                    <div class="defteryuvarlak2"></div>
                    <div class="defteryuvarlak3"></div>
                    <div class="defteryuvarlak4"></div>
                    <div class="defteryuvarlak5"></div>
                    <div class="defteryuvarlak6"></div>
                    <div class="defterteli1"></div>
                    <div class="defterteli2"></div>
                    <div class="defterteli3"></div>
                    <div class="defterteli4"></div>
                    <div class="defterteli5"></div>
                    <div class="defterteli6"></div>
                    <div class="baslik">
                        
                        <br>
                        
                    </div>
                    <div class="ucusankalp"></div>
                </div>
                <div class="arkayuz">
                    <div class="mesaj">
                        
                        <br>
                        
                    </div>
                </div>

            </div>
        </div>
    </div>
    <div id="mutluSonEkran">
        <div class="kocaman-kalp"></div>
        <div class="son-mesaj"><br></div>
    </div>
</body>

</html>
