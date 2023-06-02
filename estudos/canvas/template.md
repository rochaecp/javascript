# Canvas - Template

index.html:

~~~html
<!DOCTYPE html>
<html lang="en-us">
<head>
    <meta charset="utf-8">
    <title>Projeto</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
</head>

<body>
   
    <canvas id="myCanvas" width="400" height="200">
        O seu browser não suporta canvas!
    </canvas>

    <script src="scripts.js"></script>
</body>
</html>
~~~

styles.css:

~~~css
body {
    background-color: #282525;
    color: white;
}

#myCanvas {
    border: 1px solid #c3c3c3;
}
~~~

scripts.js:

~~~javascript
var canvas = document.getElementById('myCanvas');
// code here
~~~
