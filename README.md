## Flask Application for a Toy Ordering Website

### HTML Files

- **index.html:**
    - Main page of the website where customers can view and order toys.
    - Displays a list of available toys, each with a description, price, and Add to Cart button.

- **cart.html:**
    - Displays the customer's shopping cart, containing a list of selected toys along with their quantity, price, and total amount.
    - Provides options to modify the cart (e.g., update quantities, remove items), as well as a Checkout button.

- **checkout.html:**
    - Checkout page where customers can enter their details (e.g., name, address, payment information) to complete their order.

### Routes

- **@app.route('/')**:
    - Defines the main route for the website.
    - Renders the **index.html** file, displaying the list of toys.

- **@app.route('/cart')**:
    - Cart route that displays the customer's shopping cart.
    - Renders the **cart.html** file.

- **@app.route('/add_to_cart')**:
    - Route for adding toys to the cart.
    - Receives toy details (e.g., toy ID, quantity) and adds them to the customer's cart.
    - Redirects to the cart page.

- **@app.route('/update_cart')**:
    - Route for updating the cart.
    - Receives the toy ID and updated quantity and updates the customer's cart.
    - Redirects to the cart page.

- **@app.route('/remove_from_cart')**:
    - Route for removing toys from the cart.
    - Receives the toy ID and removes the toy from the customer's cart.
    - Redirects to the cart page.

- **@app.route('/checkout')**:
    - Checkout route that displays the checkout page.
    - Renders the **checkout.html** file.

- **@app.route('/place_order')**:
    - Order processing route that receives and validates customer details.
    - Processes the order and saves it to the database.
    - Redirects to a confirmation or order details page.