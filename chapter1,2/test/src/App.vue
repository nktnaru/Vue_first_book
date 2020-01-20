<!DOCTYPE html>
<html>
  <head>
    <title>TEST</title>
    <script src="https://unpkg.com/vue"></script>
  </head>

  <body>
    <h1>Vue.js</h1>
    <div id="app">
      {{ message }}
    </div>
    <hr />
    <button :click="doAction()">
      click
    </button>

    <input type="text" onInput="doAction(event);" />

    <script>
      var app = new Vue({
        el: "#app",
        data: {
          message: "hello world"
        }
      });

      function doAction() {
        data.message = event.target.value;
      }
    </script>
  </body>
</html>
