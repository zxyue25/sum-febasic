```
<html>
  <head>
    <title>微前端-ifame</title>
  </head>
  <body>
    <h1>我是容器</h1>
    <iframe id="mfeLoader"></iframe>
    <script type="text/javascript">
      const routes = {
        '/': 'https://app.com/index.html',
        '/app1': 'https://app1.com/index.html',
        '/app2': 'https://app2.com/index.html',
      };

      const iframe = document.querySelector('#mfeLoader');
      iframe.src = routes[window.location.pathname];
    </script>
  </body>
</html>
```
