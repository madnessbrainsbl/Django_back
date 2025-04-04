# Market Place API

A Django-based REST API for an online marketplace platform. This project provides a complete backend solution for managing products, orders, users, and shop operations.

## Features

- User authentication and authorization
- Product catalog management
- Shopping cart functionality
- Order processing
- Partner (shop) management
- Contact information management
- Swagger API documentation

## Tech Stack

- Python 3.11
- Django 5.2
- Django REST Framework
- PostgreSQL
- Swagger/OpenAPI documentation

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd market_place
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # for Linux/Mac
venv\Scripts\activate     # for Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up the database:
```bash
python manage.py migrate
```

5. Create a superuser:
```bash
python manage.py createsuperuser
```

6. Run the development server:
```bash
python manage.py runserver
```

## API Documentation

The API documentation is available at:
- Swagger UI: http://127.0.0.1:8000/swagger/
- ReDoc: http://127.0.0.1:8000/redoc/

### Main API Endpoints

1. **Users**
   - `GET/POST /api/v1/user/` - List users and registration
   - `GET/PUT/DELETE /api/v1/user/{id}/` - User details
   - `POST /api/v1/user/login/` - User login
   - `POST /api/v1/user/password_reset/` - Password reset

2. **Categories**
   - `GET /api/v1/categories/` - List categories
   - `GET /api/v1/categories/{id}/` - Category details

3. **Shops**
   - `GET /api/v1/shops/` - List shops
   - `GET /api/v1/shops/{id}/` - Shop details

4. **Products**
   - `GET /api/v1/products/` - List products
   - `GET /api/v1/products/{id}/` - Product details

5. **Basket**
   - `GET/POST /api/v1/basket/` - List items in basket and add items
   - `GET/PUT/DELETE /api/v1/basket/{id}/` - Manage items in basket

6. **Orders**
   - `GET/POST /api/v1/order/` - List and create orders
   - `GET/PUT/DELETE /api/v1/order/{id}/` - Manage orders

7. **Contacts**
   - `GET/POST /api/v1/contact/` - List and create contacts
   - `GET/PUT/DELETE /api/v1/contact/{id}/` - Manage contacts

8. **Partners**
   - `POST /api/v1/partner/update/` - Update price list
   - `GET /api/v1/partner/state/` - Check shop status
   - `GET /api/v1/partner/orders/` - Get shop orders

## Project Structure

```
market_place/
├── marketplace/
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── serializers.py
│   ├── signals.py
│   ├── urls.py
│   └── views.py
├── market_place/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── requirements.txt
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 
