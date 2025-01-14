# py-apibase

`py-apibase` is a lightweight Python library that simplifies the creation of API clients. It uses the popular `requests` library for handling HTTP requests and abstracts away much of the complexity, allowing you to focus on interacting with the API.

## Features

- Simple and intuitive interface
- Supports basic authentication and token-based authentication
- Automatically handles URL construction
- Uses Python's `requests` library for HTTP requests

## Requirements

- Python 3.x
- `requests` library

## Installation

You can install `py-apibase` using pip:

```sh
pip install py-apibase
```

## Usage

Here's a basic example of how to use apibase to create an API client:

```python
from apibase import ApiBase

BASE_URL = 'https://api-base.cloud'

class APITest(ApiBase):
    pass

fc = APITest(username="user", password="pass", key="key", token="token")

# https://api-base.cloud/orders
orders = fc.orders.get()

for order in orders:
    print(f"uid: {order.get('uid')} description: {order.get('description')}")
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
Contributing

Contributions are welcome! Please open an issue or submit a pull request.