# Personal Data

## Description
This project contains implementation of a personal data filtering system that helps in handling sensitive information in logs and databases. It includes functionality for:

- Logging message obfuscation
- Password encryption
- Database operations with sensitive data
- PII (Personally Identifiable Information) data handling

## Requirements
- All files interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All files should end with a new line
- The first line of all files should be exactly #!/usr/bin/env python3
- Code should use pycodestyle style (version 2.5)
- All files must be executable
- All modules, classes and functions should be documented

## Files
- `filtered_logger.py`: Contains logging and filtering functionality
- `encrypt_password.py`: Contains password encryption functionality

## Setup
```bash
# Install required packages
pip3 install bcrypt
pip3 install mysql-connector-python

# Set up environment variables for database connection
export PERSONAL_DATA_DB_USERNAME="your_username"
export PERSONAL_DATA_DB_PASSWORD="your_password"
export PERSONAL_DATA_DB_HOST="your_host"
export PERSONAL_DATA_DB_NAME="your_database"
```

## Usage
### Filtering Logs
```python
from filtered_logger import filter_datum

fields = ["password", "date_of_birth"]
messages = ["name=egg;email=eggmin@eggsample.com;password=eggcellent;date_of_birth=12/12/1986;"]
print(filter_datum(fields, 'xxx', messages[0], ';'))
```

### Password Encryption
```python
from encrypt_password import hash_password, is_valid

password = "MyPassword123"
hashed = hash_password(password)
print(is_valid(hashed, password))  # True
```

## Testing
Each file can be tested individually:
```bash
python3 -m doctest -v filtered_logger.py
python3 -m doctest -v encrypt_password.py
```

## Author
Silas Edet
