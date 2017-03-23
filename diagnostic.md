# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    In routes we define actions and in router we define realted extensions of the
    the action on url
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}} {{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    First route is a nested route and all component needed to be nested and product
    inherit from products. Second one is a independet route with a defined route
    actions need to be passed from inner to outter eleements
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    const id  = params.movie_id;
    return moviess.find((movie) => movie.id === +id);
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
  {{model}}
    ```
