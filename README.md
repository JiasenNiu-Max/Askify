# Askify

Askify is a Python-based backend service designed to provide RESTful APIs for question-answer platforms or Q&A systems. It is built using the Flask framework and supports deployment with Docker, CI/CD via GitHub Actions, and scalable production setup.

## 🚀 Features

- RESTful API built with Flask
- Modular project structure with clear separation of concerns
- Swagger documentation integration
- Dockerized for development and production
- CI/CD workflows via GitHub Actions
- PostgreSQL database support with backup file
- Utility functions and constants abstraction
- Test database and utility scripts

## 🗂 Project Structure

```

Askify-main/
├── app/                       # Main Flask app
│   ├── **init**.py
│   ├── constants.py
│   ├── extensions.py
│   ├── swagger.py
│   ├── utils.py
│   └── api/                   # API routes and services
│       ├── **init**.py
│       ├── routes.py
│       └── service.py
├── .github/                   # GitHub Actions workflows
│   ├── workflows/
│   └── pull\_request\_template.md
├── Dockerfile
├── docker-compose.dev.yml
├── docker-compose.prod.yml
├── requirements.txt
├── setup.py
├── run.py                     # Application entry point
├── askify\_backup.sql          # SQL backup file
├── create\_test\_db.py
├── config.ini.example
├── README.md
└── LICENSE

````

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/Askify.git
cd Askify-main
````

### 2. Setup Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Set Configuration

Copy and modify the example config:

```bash
cp config.ini.example config.ini
```

### 4. Run the Application

```bash
python run.py
```

### 5. Run in Docker

```bash
docker-compose -f docker-compose.dev.yml up --build
```

## 🧪 Testing

```bash
python test.py
```

Or setup and use a dedicated test database:

```bash
python create_test_db.py
```

## 🔄 Deployment

* Dockerized for production using `docker-compose.prod.yml`
* GitHub Actions CI/CD workflows in `.github/workflows/`
* Compatible with Render or similar platforms (see `render.yaml`)

## 📄 License

This project is licensed under the terms of the MIT License.

---

## 📌 Notes

* Swagger API documentation is provided via `swagger.py`
* Backup SQL file: `askify_backup.sql` can be used to seed your database

