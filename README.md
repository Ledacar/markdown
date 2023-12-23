#  Repositorio para saber como utilizar MARKDOWN

> convertimos con shadow el markdown y lo pintamos con JS

## Funcion para convertir y pintar en HTML
``` javascript
const app = document.querySelector('#app')
const md = fetch("post/test.md").then((response) => response.text()).then(text => {
    const converter = new showdown.Converter()
    const html = converter.makeHtml(text)
    app.innerHTML = html
})
```

## HTML
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi primer web markdown</title>
</head>
<body>
<div id="app"></div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/showdown/2.1.0/showdown.min.js"></script>
<script src="index.js"></script>
</body>
</html>
```

## Como se visualiza en el HTML

![Imagen del resultado](/img/evi.png)

## Documentacion de Scalar para probar

[Scalar](https://github.com/scalar/scalar?tab=readme-ov-file#getting-started1 "Documentacion Scalar (GIT HUB)")

