# Amazon Clone

This repository contains a front-end clone of the Amazon e-commerce website. The project is built using vanilla HTML, CSS, and JavaScript, focusing on creating a responsive and interactive user experience. It simulates key features of an e-commerce platform, including product browsing, a shopping cart, and a checkout process.

## Features

-   **Product Catalog:** A responsive grid layout displays products fetched from a mock backend service.
-   **Shopping Cart:** Users can add products to their cart. The cart quantity is updated in the header and persists across pages using `localStorage`.
-   **Checkout Process:** A multi-step checkout page that includes:
    -   Reviewing items in the cart.
    -   Updating or deleting items.
    -   Choosing from multiple delivery options.
    -   A dynamic payment summary that calculates item costs, shipping, tax, and the final total.
-   **Order Placement:** Simulates placing an order by sending cart data to a mock backend endpoint and redirects to an order history page.
-   **Order History:** A dedicated page to view previously placed orders.
-   **Package Tracking:** A simple page to visualize the shipment status of an ordered product.

## Tech Stack

-   **Frontend:** HTML5, CSS3, JavaScript (ES6+ Modules)
-   **Styling:** Responsive design implemented with CSS Grid, Flexbox, and Media Queries.
-e   **State Management:** Browser `localStorage` is used to persist cart and order data.
-   **APIs & Libraries:**
    -   **Day.js:** For date manipulation and formatting delivery dates.
    -   **Fetch API:** To asynchronously retrieve product data and post order information.
    -   **Mock Backend:** Interacts with `https://supersimplebackend.dev` to fetch products and simulate order creation.

## Project Structure

The repository is organized into distinct directories for clarity and maintainability.

```
/
├── amazon.html               # Main product listing page
├── checkout.html             # Shopping cart and checkout page
├── orders.html               # Order history page
├── tracking.html             # Order tracking page
│
├── data/                     # JavaScript modules for data management (cart, products, orders)
├── images/                   # All static image assets (products, icons, ratings)
├── scripts/                  # Page-specific JavaScript and utility functions
│   ├── checkout/             # Scripts specific to the checkout page (order summary, payment summary)
│   └── utils/                # Reusable utility scripts (e.g., money formatting)
│
└── styles/                   # CSS stylesheets
    ├── pages/                # Page-specific styles
    └── shared/               # Global and shared component styles (header, general styling)
```

## Getting Started

To run this project locally, you can simply clone the repository and open the HTML files in your browser.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/kamlesh079/Amazon-Clone.git
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd Amazon-Clone
    ```

3.  **Run the application:**
    Since the project uses ES Modules, it must be served by a local web server to work correctly.

    -   **Using VS Code Live Server:** If you have Visual Studio Code with the "Live Server" extension, you can right-click `amazon.html` and select "Open with Live Server".
    -   **Using a simple Python server:**
        ```sh
        # If you have Python 3.x
        python -m http.server

        # If you have Python 2.x
        python -m SimpleHTTPServer
        ```
    Then, open your web browser and navigate to `http://localhost:8000/amazon.html`.
