# wings_cart Cart Order Form sample

## Overview

This is the Node.js/Express.js version Cart order form.

## Structure

```
templates/orderforms/themetags_cart/
├── theme.yaml              # Order form metadata
├── thumbnail.gif           # Preview thumbnail
├── common.ejs              # Common includes (CSS/JS)
├── products.ejs            # Product listing page
├── checkout.ejs            # Checkout page (to be converted)
├── complete.ejs            # Order completion page (to be converted)
├── sidebar-categories.ejs  # Sidebar navigation
├── sidebar-categories-collapsed.ejs  # Mobile sidebar
├── sidebar-categories-selector.ejs   # Category selector
├── recommendations-modal.ejs         # Product recommendations modal
├── includes/
│   └── product-recommendations.ejs   # Product recommendations
└── assets/
    ├── css/                # Theme stylesheet (custom.css)
    ├── js/                 # Theme JavaScript (if any)
    └── img/                # Images
```



### Data Structure

The controller provides the following data to templates:
- `user` - Current user object
- `form` - Order form metadata
- `step` - Current step (products, checkout, etc.)
- `formId` - Order form ID
- `lang` - Language translations object
- `productGroup` - Current product group
- `products` - Array of products
- `secondarySidebar` - Sidebar navigation data
- `currencies` - Available currencies
- `currency` - Current currency

## Usage

### Access Order Form

```
GET /orderforms/wings_cart?step=products
```

### Available Steps

- `products` - Product listing (default)
- `checkout` - Checkout page
- `complete` - Order completion
- `viewcart` - View cart
- `configure` - Configure product
- `configuredomain` - Configure product with domain

### Static Assets

Assets are served from:
```
/orderforms/wings_cart/assets/{path}
```

## Templates

- [ ] `checkout.ejs` - Checkout form
- [ ] `complete.ejs` - Order completion
- [ ] `viewcart.ejs` - Shopping cart view
- [ ] `configureproduct.ejs` - Product configuration
- [ ] `configureproductdomain.ejs` - Product with domain configuration
- [ ] `configuredomains.ejs` - Domain configuration
- [ ] `domainregister.ejs` - Domain registration
- [ ] `domaintransfer.ejs` - Domain transfer
- [ ] `domainrenewals.ejs` - Domain renewals
- [ ] `addons.ejs` - Product addons
- [ ] `linkedaccounts.ejs` - Linked accounts
- [ ] `ordersummary.ejs` - Order summary
- [ ] `error.ejs` - Error page
- [ ] `fraudcheck.ejs` - Fraud check page

## Dependencies

- Bootstrap 3 or 4
- jQuery 1.12+
- Font Awesome 5

## Notes

- The form uses EJS templating engine
- Asset paths are relative to the order form assets route
- Language keys should be provided via the `lang` object in template data

