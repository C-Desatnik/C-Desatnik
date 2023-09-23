  <html>
  <head>
 <style>
   body{
     background-color:black;
   }
   .TS{
     margin-top:50px;
   }
   .BS{
     margin-bottom:100px;
   }
   </style>
  </head>
    <body>
      <script>
            function play(game) {
                "use strict";
                document.querySelector("#nav li a.selected").className = "";
                document.querySelector(`#nav li a[data-game=${game}]`).className = "selected";
                document.getElementById("title").innerHTML = game;
                document.getElementById("machine").src = `${game}/index.html`;
                document.title = "HTML5 Games: " + game.substring(0, 1).toUpperCase() + game.substring(1);
            }

            window.addEventListener("load", () => {
                "use strict";
                const header = document.querySelector("header");
                play(location.hash.substring(1) || "bounce");
                document.querySelector("#nav").addEventListener("click", (e) => {
                    if (e.target.dataset.game) {
                        play(e.target.dataset.game);
                    }
                });
            }, false);
        </script>
<form action="index.html">
      <center><button type="submit" class="button" class="TS">HOME</button></center>
       </form>
      <br>
   <center><a href="#Game-1" data-game="tetris"><button>Tetris</button></a></center>
      <br>
      <center><a class="BS" href="https://www.kanogames.com/profile/developer/bored-dot-com"> <button>Bored</button> </a></center>
  </body>
  </html>
