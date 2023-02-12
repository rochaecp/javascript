# Dark Mode

Em um navegador, ao tentar visualizar um PDF você pode abrir o console e executar o seguinte código:

~~~javascript
function togglePDFDarkMode() {
  var cover = document.createElement("div");
  let inversion = `
    position: fixed;
    pointer-events: none;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: #dedede;
    mix-blend-mode: difference;
    z-index: 1;
    `
  if (document.body.contains(cover)) {
    document.body.removeChild(cover);
  } else {
    cover.setAttribute("style", inversion);
    document.body.appendChild(cover);
  }
}
togglePDFDarkMode();
~~~
