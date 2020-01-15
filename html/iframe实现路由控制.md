
iframe天然具备微前端基因，只需将单体的前端应用，按照业务模块进行拆分，分别部署，最后通过iframe动态加载
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
优点：实现简单、天然具备隔离性
缺点：主页面和iframe共享最大允许的http链接数、iframe阻塞主页面加载、浏览器的后退按钮无效
