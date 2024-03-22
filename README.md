# Installation Instructions for Django Backend SupportPlus Application
Made by Nic Tauroa and Matt Taylor

## Note: Yoobee Instructors 

This project contains a sample sqlite.db file
This contains our testing data and users so that the local application can be used and tested showcasing our project.

The below instructions are to meet the assesment criteria for installing the application for the user.
---

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- Python 3.8 or higher
- pip (Python package installer)

## Setting Up Your Environment

1. **Clone the Repository**

   First, clone the application repository to your local machine using Git:

   ```bash
   git clone https://yourrepositoryurl.git
   cd path/to/your/project
   ```

   Replace `https://yourrepositoryurl.git` with the URL of your Git repository.

2. **Create a Virtual Environment**

   It's a good practice to create a virtual environment for your project to manage dependencies. Run the following command in the root directory of your project:

   ```bash
   python -m venv venv
   ```

   Activate the virtual environment:

   - On Windows:

     ```cmd
     .\venv\Scripts\activate
     ```

   - On macOS and Linux:

     ```bash
     source venv/bin/activate
     ```

3. **Install Dependencies**

   Install the required packages using `pip`:

   ```bash
   pip install -r requirements.txt
   ```

## Configuring the Application

1. **Environment Variables**

   Set up the necessary environment variables, if any, required by your application. This might include database configurations, secret keys, and third-party API keys.

   Create a `.env` file in the root directory of your project and populate it with your environment variables:

   ```plaintext
   SECRET_KEY=your_secret_key
   DEBUG=True
   DATABASE_URL=your_database_url
   ```

2. **Database Migrations**

   Apply database migrations to set up your database schema:

   ```bash
   python manage.py migrate
   ```

3. **Create an Admin User**

   Create a superuser account for Django's admin:

   ```bash
   python manage.py createsuperuser
   ```

   Follow the prompts to set up the username, email, and password for the superuser.

## Running the Development Server

1. **Start the Server**

   Run the Django development server:

   ```bash
   python manage.py runserver
   ```

2. **Access the Application**

   Open your web browser and navigate to `http://localhost:8000` to view the application. Access the Django admin site at `http://localhost:8000/admin` using the superuser account you created.

## Additional Configuration

- For additional configurations such as setting up email backends, caching, or static files handling for production, refer to the Django documentation and customize your `settings.py` file accordingly.

---

Ensure to replace placeholders like `your_repository_url`, `your_secret_key`, `your_database_url`, etc., with actual values relevant to your project. This guide provides a general approach to setting up a Django backend application, and specific details may vary based on your project's requirements.