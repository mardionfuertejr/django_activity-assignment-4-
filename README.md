# Django Library App

A simple Django web application for managing a library with books, authors, and categories.

## Features

- **Books**: Manage book information including title, author, categories, and publication date
- **Authors**: Add and manage author information
- **Categories**: Organize books by categories (Fantasy, Fiction, Classic, etc.)
- **Admin Interface**: Full Django admin interface for easy data management
- **Web Interface**: Clean display of all books and categories

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd assignment-4
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Main website: http://127.0.0.1:8000/
   - Admin interface: http://127.0.0.1:8000/admin/

## Usage

### Adding Data

1. Go to the admin interface: http://127.0.0.1:8000/admin/
2. Login with your superuser credentials
3. Add authors, categories, and books in the Library section

### Viewing Data

Visit the main page (http://127.0.0.1:8000/) to see all books and categories displayed in a clean format.

## Project Structure

```
assignment-4/
├── manage.py
├── requirements.txt
├── README.md
├── .gitignore
├── library_project/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── library/
    ├── models.py      # Author, Category, Book models
    ├── admin.py       # Admin interface configuration
    ├── views.py       # Home view
    ├── urls.py        # URL routing
    └── templates/
        └── home.html  # Main page template
```

## Models

- **Author**: Stores author names
- **Category**: Stores book categories (Fantasy, Fiction, etc.)
- **Book**: Stores book information with relationships to authors and categories

## Security Notes

- The `settings.py` file contains sensitive information and should not be committed to version control
- Use environment variables for production deployments
- Never commit `db.sqlite3` or other database files

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is for educational purposes.
