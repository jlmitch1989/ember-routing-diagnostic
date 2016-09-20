# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The Router works a lot like the routes.js file in rails.  It handles
    all of the needed routes for your ember application.  The Ember Route
    file handles the data from the API.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{link-to 'boston' boston}}
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
    { path: '/:product_id' }
     - This is a specific product of the product route.

     { path: '/products/:product_id' }
     -Of product there are many products and each product has an id.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    I'm not sure I understand the question completely, but I'm guessing with
    passing `params`?
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    By refrencing the model within the #each.  For example:

    {{#each model as |list|}}
      {{listr-list/card list=list}}
    {{/each}}
    ```
