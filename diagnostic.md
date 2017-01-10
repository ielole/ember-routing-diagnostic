# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The Router, parses the url and directs the user/client/browser to the
    appropriate route.

    The Route sends and recieves data from the server.

    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to campus/boston}}{{/link-to}}
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
    1.)In the first route, the product folder is nested inside of the products folder.
    2.)The paths for when the product route ('product') is accessed are
    different. The urls would be different. 
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    The value can be referenced as movie.movie_id.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Assign the data to a variable and pass the variable to a component.
    ```
