<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>carte de Visite</title>
    <link rel="stylesheet" href="carteVisite.css">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>

</head>

<body>
    <h1 id="indicator">Enter your informations then click Enter to get your Visitcarrd</h1>
    <div class="formulaire">
        <form>
            <label for="nom">Enter your first and last name</label> <br>
            <input type="text" name="nom" id="nom"> <br>

            <label for="fonction">Enter your position</label> <br>
            <input type="text" name="fonction" id="fonction"> <br>

            <label for="rue">roadname and housenumber</label> <br>
            <input type="text" name="rue" id="rue"> <br>

            <label for="plz">Your official P.O. Box and city</label> <br>
            <input type="text" name="plz" id="plz"> <br>
            <label for="mail">Your professional email</label><br>
            <input type="email" name="mail" id="mail">
            <br>
            <label for="entreprise">Name of your Enterprise</label> <br>
            <input type="text" name="entreprise" id="entreprise"> <br>
            <label for="logo">optional. add your logo</label> <br>
            <input type="file" name="logo" id="logo"> <br>

            <label for="execute">Click Enter to get your visitcard</label> <br>
            <input type="button" id="execute" value="Enter">
        </form>
    </div>

    <div class="finition">
        <div class="cartefini">
            <div class="case case1">
                <div class="item name">Nom Prenom</div>
                <div class="item fonction">Fonction <br></div>
            </div>

            <div class="case">
                <div class="item image">
                    <img src="" alt="">
                </div>
                <div class="item contact"><span id="road">Contact</span> <br>
                    <span id="poBox"></span> <br>
                    <span id="email">E-Mail</span>
                </div>


            </div>
        </div>
        <div class="entreprise">Nom de l´Entreprise e.V </div>

    </div>

    <script>
        var rue;
        var plz;
        var mail;

        $("#execute").click(function(e) {
            rue = document.getElementById("rue").value;
            plz = document.getElementById("plz").value;
            mail = document.getElementById("mail").value;
            var contactDaten = rue + "<br>" + plz + "<br>" + mail;

            e.preventDefault();
            $(".name").text($("#nom").val());
            $(".fonction").text($("#fonction").val());
            $(".fonction").css("color", "#540054");
            $("#road").text($("#rue").val());
            $("#poBox").text($("#plz").val());
            $("#email").text($("#mail").val());
            $(".entreprise").text($("#entreprise").val());

            $(".formulaire").fadeOut(2000, function() {
                $("#indicator").text("Thank you for using our express Visitcard form");
                $("#indicator").css("color", "white");
                $("#indicator").css("font-size", "2em");

            }), $(".finition").fadeIn(2000);


        })
    </script>

</body>

</html>
