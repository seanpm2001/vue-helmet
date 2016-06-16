# vue-helmet

This is a [Example Demo](//miaolz123.github.io/vue-helmet/) of vue-helmet

```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Something old." />
  <style type="text/css">
    .v-link-active {
      color: red;
    }
  </style>
</head>

<body>
  <vue-helmet title="App" />
  <h1>Hello App!</h1>
  <p>
    <a v-link="{ path: '/foo' }">Go to Foo</a>
    <a v-link="{ path: '/bar' }">Go to Bar</a>
  </p>
  <router-view></router-view>
  <hr>
  <p>
    Powered by <a href="//github.com/miaolz123/vue-helmet" target="_blank">VueHelmet</a>
  </p>
  <script type="text/javascript" src="dist/vue.js"></script>
  <script type="text/javascript" src="dist/vue-router.js"></script>
  <script type="text/javascript" src="dist/vue-helmet.js"></script>
  <script>
    var App = Vue.extend({});
    var Foo = Vue.extend({
      template: "<vue-helmet title='Foo' /><p>This is foo!</p>"
    });
    var Bar = Vue.extend({
      template: "<vue-helmet title='Bar' /><p>This is bar!</p>"
    });
    var router = new VueRouter();

    Vue.use(VueHelmet);
    router.map({
      "/foo": {
        component: Foo
      },
      "/bar": {
        component: Bar
      }
    });
    router.start(App, "body");
  </script>
</body>

</html>
```

# License

Copyright (c) 2016 [miaolz123](https://github.com/miaolz123) by [MIT](https://opensource.org/licenses/MIT)