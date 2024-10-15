# [DobyEmail](python.dobyemail.com)

This project contains a set of Python classes and utilities for handling email operations.

## Project Structure

```
python.dobyemail.com/
├── src/
│   └── dobyemail/
│       ├── __init__.py
│       ├── config.py
│       ├── email_ports.json
│       ├── service.py
│       ├── sender.py
│       ├── reader.py
│       ├── transfer.py
│       ├── parse_date.py
│       ├── check_ports.py
│       ├── is_valid_email.py
│       └── get_email_ports.py
├── tests/
│   └── test_email_utils.py
├── README.md
├── requirements.txt
└── setup.py
```

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/dobyemail/python.git
   ```

2. Change to the project directory:
   ```
   cd dobyemail
   ```

3. Install the package:
   ```
   pip install .
   ```

## Usage

Import the necessary classes from the package to use in your project. For example:

```python
from dobyemail import Service, config

# Initialize the email service
service = Service(
    smtp_server=config.smtp_server,
    smtp_port=config.smtp_port,
    smtp_use_tls=config.smtp_use_tls,
    imap_server=config.imap_server,
    imap_port=config.imap_port,
    imap_use_ssl=config.imap_use_ssl,
    username=config.username,
    password=config.password
)

# Use the service methods for reading or sending emails
service.send_email(to_email, subject, body)
```

## Running Tests

To run the unit tests, use the following command from the project root directory:

```
python -m unittest discover tests
```

## Configuration

The `email_ports.json` file is used for configuring email ports. It is loaded automatically by the `Config` class in `config.py`.

## Contributing

Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
