# ![Tux, the Linux mascot](./asset/Instagram_icon-icons.com_66804.png) TP Instagram 
## SERRARI Jalal SIO SLAM 2
```html
<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Copie Instagram</title>
    <link rel="stylesheet" href="./css/style.css">
    <link rel="icon" type="image/png" sizes="32x32" href="./asset/Instagram_icon-icons.com_66804.png">
</head>

<body>

    <header>
        <h1>Réalisation d'une copie de la page de connexion du site <span class="insta">Instagram</span></h1>
    </header>

        <main>

            <div class="form" >
                <img src="./svg/logo_instagram.svg" alt="Instagram" class="logo">
                <p></p>

                    <form action="accueil.html" method="get">
                        <input type="email" placeholder="Mail Utilisateur" name="mail"  id="email" aria-required="true">
                        <input type="password" placeholder="Mot de passe" name="password"  id="password" aria-required="true">
                        <input type="submit" value="Se connecter">
                    </form>
                    
                    <p class="ou">OU</p>
                    <hr>
                    
                    <ul>
                        <li class="face"><p><a href="https://www.facebook.com/login.php?skip_api_login=1&api_key=124024574287414&kid_directed_site=0&app_id=124024574287414&signed_next=1&next=https%3A%2F%2Fwww.facebook.com%2Fdialog%2Foauth%3Fclient_id%3D124024574287414%26redirect_uri%3Dhttps%253A%252F%252Fwww.instagram.com%252Faccounts%252Fsignup%252F%26state%3D%257B%2522fbLoginKey%2522%253A%252214vvp4ixiwzacuxq2rqck8i5s1cyoq9qairxe49rqg2o1qzp6vc%2522%252C%2522fbLoginReturnURL%2522%253A%2522%252Ffxcal%252Fdisclosure%252F%253Fnext%253D%25252F%2522%257D%26scope%3Demail%26response_type%3Dcode%252Cgranted_scopes%26locale%3Dfr_FR%26ret%3Dlogin%26fbapp_pres%3D0%26logger_id%3D8192b253-d0bd-4425-beec-188ef98b8351%26tp%3Dunspecified&cancel_url=https%3A%2F%2Fwww.instagram.com%2Faccounts%2Fsignup%2F%3Ferror%3Daccess_denied%26error_code%3D200%26error_description%3DPermissions%2Berror%26error_reason%3Duser_denied%26state%3D%257B%2522fbLoginKey%2522%253A%252214vvp4ixiwzacuxq2rqck8i5s1cyoq9qairxe49rqg2o1qzp6vc%2522%252C%2522fbLoginReturnURL%2522%253A%2522%252Ffxcal%252Fdisclosure%252F%253Fnext%253D%25252F%2522%257D%23_%3D_&display=page&locale=fr_FR&pl_dbl=0"><i class="fa fa-facebook-official" aria-hidden="true"><img src="./asset/Facebook.png" alt="Facebook"></i> &nbsp;&nbsp;<strong>Se connecter avec Facebook</strong></a></p></li>
                        <li><p><a href="https://www.instagram.com/accounts/password/reset/?hl=fr">Mot de passe oublié ?</a></p></li>
                    </ul>
            </div>

```
```css
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700;800&display=swap');
html{
    font-size: 62.5%;
    scroll-behavior: smooth;
}
body{
    font-size: 1.6rem;
    font-family: 'Open Sans', sans-serif;
    margin: 0;
    background-color: #fafafa;
}
h1, h2, h3, h4, h5, h6, p, figure, ul, ol{
    margin: 0;
    padding: 0;
    list-style: none;
}
a{
    color: #222;
    text-decoration: none;
}
*{
    box-sizing: border-box;
}
button{
    padding: 0;
    border: 0;
    background-color: transparent;
}

/* header */
header{
    padding: 2rem;
    text-align: center;
    background-color: #fafafa;
}
header h1{
    text-transform: uppercase;
    color: #545454;
    font-size: 100%;
}
header h1 .insta{
    color: #222;
}

/*main*/
main{
    padding : 1rem;
}
.form{
    border: solid 0.2rem #cecece;
    margin: 1rem auto;
    padding: 4rem;
    max-width: 37rem;
    margin: 1rem auto;
    max-width: 37rem;
    background-color: #fff;
    display: block;

}
```
```js
document.addEventListener("DOMContentLoaded", () => {

    console.log("chargé");
    let btn, warning, email, password;
    let exprmail = /^[a-zA-Z0-9._-]+@[a-z0-9._-]{2,}\.[a-z]{2,4}$/;
    let exprmdp = /^[a-zA-Z0-9._-]{2,15}$/;

    warning = document.querySelector(".form p");
    email = document.getElementsByTagName("input")[0].value;
    password = document.getElementsByTagName("input")[1].value;
    btn = document.getElementsByTagName("input")[2];

    btn.addEventListener("click", e => {

        e.preventDefault();
        formActive();
    });
    let formActive = () => {

        email = document.getElementsByTagName("input")[0].value;
        password = document.getElementsByTagName("input")[1].value;
        if (email.match(exprmail) && password.match(exprmdp)) {

            warning.classList.add("success");
            warning.classList.remove("error");
            warning.innerText = "Connexion réussie";
            localStorage.setItem("user", email);
            sessionStorage.setItem("user", "sessionid");
            document.location.assign("accueil.html");

        } else if (email.match(exprmail)) {

            warning.classList.add("error");
            warning.innerText = "Mot de passe invalide";
            warning.classList.remove("success");
        } else {

            warning.classList.add("error");
            warning.innerText = "Mail ou mot de passe incorrecte";
            warning.classList.remove("success");
        };
```
## Les notions développement
* HTML<sup>5</sup>
* CSS<sub>3</sub>
* JS

Voir la page web *[https://katshoww.github.io/Instagram_SERRARI/]()*.