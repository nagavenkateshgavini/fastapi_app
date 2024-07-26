# fastapi_app

# FastAPI Application

This project is a FastAPI application that serves as the backend API. It includes endpoints to retrieve company information and locations from CSV files.

## Features

- Get all companies
- Get company details by ID
- Get all locations for a specific company ID
- Basic error handling
- Logging

## Endpoints

### Get All Companies

- **URL**: `/companies`
- **Method**: `GET`
- **Description**: Retrieves a list of all companies.
- **Response**: JSON array of companies

### Get Company Details by ID

- **URL**: `/companies/{company_id}`
- **Method**: `GET`
- **Description**: Retrieves details of a specific company by its ID.
- **Response**: JSON object of company details

### Get All Locations for a Specific Company ID

- **URL**: `/companies/{company_id}/locations`
- **Method**: `GET`
- **Description**: Retrieves all locations for a specific company ID.
- **Response**: JSON array of locations

## Directory Structure
```commandline
.
├── README.md
├── data
│   ├── companies.csv
│   └── locations.csv
├── exceptions
│   └── custom_exceptions.py
├── main.py
├── models
│   ├── company.py
│   └── location.py
├── postman_collection
│   └── collection.json
├── requirements.txt
├── routers
│   ├── companies.py
│   └── locations.py
├── services
│   ├── company_service.py
│   └── location_service.py
└── utils
    └── logger.py
```

### File Descriptions
- **main.py:** The entry point of the application. It sets up the FastAPI app and includes the routers.
- **routers/companies.py:** Contains endpoints related to companies.
- **routers/locations.py:** Contains endpoints related to locations.
- **models/company.py:** Defines the Company model using Pydantic.
- **models/location.py:** Defines the Location model using Pydantic.
- **services/company_service.py:** Contains logic for fetching company data from companies.csv.
- **services/location_service.py:** Contains logic for fetching location data from locations.csv.
- **data/companies.csv:** The CSV file containing company data.
- **data/locations.csv:** The CSV file containing location data.
- **exceptions/custom_exceptions.py:** Defines custom exceptions for the application.
- **utils/logger.py:** Sets up the logging configuration.



## Setup

### Prerequisites

- Python 3.9+
- pip

### Installation

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
   cd fastapi_app

2. **Create a virtual environment**:

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3. **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Run the application:**

    ```bash
    uvicorn main:app --reload
    ```

### API Documentation:

FastAPI automatically generates interactive API documentation. You can access it at:

**Swagger UI:** http://127.0.0.1:8000/docs

**ReDoc:** http://127.0.0.1:8000/redoc

### Error Handling
The application includes basic error handling and custom exceptions to ensure robust API responses.

### Logging
Logging is set up using Python's built-in logging module, providing insight into the application's operation and potential issues.

### Contributing
Feel free to submit issues, fork the repository, and send pull requests. We appreciate any help in improving the application.

### License
This project is licensed under the MIT License.


