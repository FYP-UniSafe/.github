# ONLINE GENDER-BASED VIOLENCE INFORMATION SYSTEM (UniSafe)

You can find a Preview of all this README at https://github.com/FYP-UniSafe/.github.git

## TEAM MEMBERS

| Registration Number | Name                  | Role                                                                  |
| ------------------- | --------------------- | --------------------------------------------------------------------- |
| 2021-04-05717       | Mandy, Nuhu Paschal   | Backend (Web and Mobile) Frontend (Scripting, Modules and Services - Web App) |
| 2021-04-07667       | Mollam, Reuben Wiliam | Frontend (Mobile App) & UI Designer (Mobile App)                      |
| 2021-04-05873       | Mariki, Whitney       | Frontend (HTML and CSS - Web App) & UI Designer (Web App)           |
| 2021-04-09212       | Musama, Irene         | Text Message Application                                              |

## INTRODUCTION

This project focuses on addressing GBV within the University of Dar es Salaam (UDSM) by developing an Online Gender-Based Violence Information System. The system aims to provide a safe and supportive environment for
students to report incidents and access support services (counseling) and visualize data related to GBV cases.

### Main Features

- GBV Cases Reporting (Anonymous and Normal Reporting)
- Gender Desk Functionalities (Accepting, Rejecting, Forwarding and Closing Reports)
- Counseling (Online and Physical appointments and AI-driven sessions)
- Statistics, Maps and Data Visualization
- Police Functionalities (Accepting forwarded reports, Closing Reports)

### Modules

The project encompasses the development of a comprehensive system that includes a Mobile
application, a Web-based application and offline incident reporting mechanisms using a Text
message application.

### Technologies Used

**Frontend Mobile**

- Flutter
- Dart programming language
- Google Maps API for geolocation
- VideoSDK for Video calls

**Frontend Mobile**

- Angular Framework
- HTML, CSS, JavaScript and Typescript
- Google Maps API for geolocation
- VideoSDK for Video calls
- ChatsJS for Data Visualisation

**Backend**

- Django
- Python Programming Language

**UI&UX**

- Figma for mockups, wireframes and final designs

## UniSafe MOBILE FRONTEND

This section explains how to set up and run UniSafe App in Android studio

### Prerequisites

1. [Flutter (3.14 or higher)](https://flutter.dev/), can be updated by running `flutter upgrade`
2. git

### Setup

Clone repository

```bash
 git clone https://github.com/FYP-UniSafe/frontend-mobile.git
```

Clear Any Cache

```bash
flutter clean
```

Install all required dependencies for the app

```bash
flutter pub get
```

### Development

Duplicate .env.example and rename the copied file to .env and add the required values in the .env

```bash
cp .env.example .env
```

1. Add the Google Maps API Key to the [AppDelegate.swift](/ios/Runner/AppDelegate.swift) in the runner folder in the ios directory. Replace `api_key_here` with your API Key

2. Add the Google Maps API Key to the [AndroidManifest.xml](/android/app/src/main/AndroidManifest.xml) in the android app directory. Replace `api_key_here` with your API Key

Run the app on the available emulator/device

```bash
flutter run
```

### Build

After making the changes we build the application by following the steps below:

Run the following command to build the application for android

```bash
flutter build apk
```

### Contributing

Contributions are welcome. Please follow our guidelines...

### License

This project is licensed under the [MIT License](LICENSE).

### Contact

For inquiries, contact [Reuben William Mollam](mailto:euphoricreuben@gmail.com).

## UniSafe WEB FRONTEND

### Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js**: The runtime environment for running JavaScript on the server side. This project requires Node.js version 18.19.0. Download and install it from [Node.js official website](https://nodejs.org/).

- **Angular CLI**: The command-line interface tool that you use to initialize, develop, scaffold, and maintain Angular applications. This project uses Angular CLI version 17.3.8. Install it globally via npm:

```bash
  npm install -g @angular/cli@17.3.8
```

- **Angular Framework**: This project is developed with Angular version 17.3.10. Ensure that your Angular CLI is compatible with this version by installing the specific version of Angular CLI mentioned above.

- **Git**: Version control system for tracking changes in source code during software development. Download and install it from [Git's official website](https://git-scm.com/).

### Setup

To install and set up the project, follow these steps:

1. **Clone the repository:**

```bash
   git clone https://github.com/FYP-UniSafe/Frontend_Web.git
```

2. **Navigate to the project directory:**

```bash
   cd UniSafe
```

3. **Install dependencies:**

```bash
   npm install
```

4. **Serve the application:**

```bash
   ng serve
```

This command will compile the application and start a web server. By default, the application will be available at `http://localhost:4200/`.

5. **Open your browser and navigate to `http://localhost:4200/` to view the application.**

### Development to Vercel (Shared Hosting was used)

To deploy the Angular project to Vercel, follow these steps:

1. If you haven't already, install the Vercel CLI globally:

```bash
   npm i -g vercel
```

2. Navigate to the root of your project directory.
3. Run the following command to deploy your project to Vercel:

```bash
   vercel deploy --prod
```

This command deploys your project and provides you with a production URL. Follow the prompts in your terminal to set up your project on Vercel the first time you run it.

For more detailed instructions and configuration options, refer to the [Vercel documentation](https://vercel.com/docs).

### Contributing

**Contact**
For inquiries, contact [Mandy, Nuhu Paschal](mailto:caljr9301@gmail.com) or [Mariki, Whitney](mailto:marikiwhitney@gmail.com).

## UniSafe BACKEND

### Prerequisites

Before you begin, ensure you have met the following requirements for the Django backend:

- **Python**: The project requires Python 3.8 or newer. Ensure you have the correct version of Python installed on your system.

- **PostgreSQL**: This project uses PostgreSQL. Ensure you have PostgreSQL version 12 or newer installed and running on your system.

- **Virtual Environment**: It's recommended to use a virtual environment for Python projects to manage dependencies.

- **Dependencies**: Install all the dependencies listed in your `requirements.txt`.

Ensure these prerequisites are met to successfully set up and run the Django backend of your application.

### Setup

1. **Clone the repository:**

```bash
   git clone https://github.com/FYP-UniSafe/UniSafe_Backend.git
```

2. **Create and Activate the virtual env:**

```bash
    python -m venv env && source env/bin/activate
```

3. **Install the development dependencies:**

```bash
    pip install -r requirements/dev.txt
```

4. **Configure Pre-commit (Optional):**

```bash
    pre-commit install && pre-commit run --all-files
```

5. **Navigate to the project directory:**

```bash
    cd Unisafe
```

6. **Apply Migrations:**

```bash
    python manage.py migrate
```

7. **Create a superuser:**

```bash
    python manage.py createsuperuser
```

8. **Run the development server:**

```bash
    python manage.py runserver
```

9. **Open your browser and navigate to `http://localhost:8000/` to view the application and view the `OpenAPI` swagger docs.**

### Setting Up Postgres on Django Project

To set up PostgreSQL on a Linux system, you will need to do the following steps:

1. **Install the PostgreSQL package:**

```bash
sudo apt-get install postgresql postgresql-contrib
```

2. **Start the PostgreSQL service:**

```bash
sudo service postgresql start
```

3. **Log in to the PostgreSQL command-line interface as the postgres user:**

```bash
sudo -u postgres psql
```

4. **Create a new database and user:**

```bash
CREATE DATABASE yourdatabasename;

CREATE USER youruser WITH PASSWORD 'yourpassword';

GRANT ALL PRIVILEGES ON DATABASE yourdatabasename TO youruser;
```

> **Note**: Dont use the username `user` as it will conflict with the command

5. **Exit the PostgreSQL command-line interface:**

```bash
\q
```

6. **Update the Django settings to use the new database:**

```python
# settings.py

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'yourdatabasename',
        'USER': 'youruser',
        'PASSWORD': 'yourpassword',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### Contributing

**Contact**
For inquiries, contact [Mandy, Nuhu Paschal](mailto:caljr9301@gmail.com).

## UniSafe TEXT MESSAGE APPLICATION

### Prerequisites

Before setting up the text message application, ensure you have understood its purpose, the problem it solves, and the technologies used. Here's a brief overview:

### General Information

- **Purpose**: The application facilitates SMS communication through a shared shortcode, focusing on keyword-based messages for gender-based violence support.
- **Problem Solved**: It simplifies SMS-based interactions and integrates with a shared database for seamless data management and resource delivery, enhancing support mechanisms for gender-based violence.

### Technologies Used

- **Platform**: The application utilizes the TextIt platform, an online platform for managing SMS flows and interactions.
- **API**: Integration with Africa's Talking API is essential for sending and receiving SMS messages.
- **Database**: A shared database is used for both the website and the app, with data being sent in JSON format for consistency and ease of integration.

### Specific Requirements

- **TextIt Platform**: Access to the TextIt platform is required. The flow for the application can be found at [TextIt Flow Editor](https://textit.com/flow/editor/11f87f51-3784-4c31-9033-f68369dcec39/). Login credentials will be necessary for accessing the Unisafe flow.
- **Africa's Talking API**: Ensure you have valid credentials for Africa's Talking API for SMS integration.
- **Database Configuration**: The database should be configured to receive JSON data, ensuring seamless communication and data storage.

Ensure these prerequisites are met to successfully set up and run the text message application for gender-based violence support.

### Setup

#### TextIt Configuration

- Access the TextIt platform to manage SMS flows and interactions.
- Navigate to the Unisafe flow using the following link: [Unisafe Flow](https://textit.com/flow/editor/11f87f51-3784-4c31-9033-f68369dcec39/).
- For the Login Credentials (Username & Password), contact [Musama, Irene](mailto:irenemwita24@gmail.com).
  > NOTE: The shared shortcode is available for testing without requiring login credentials.

#### Database Setup

- Configure the database to accept JSON formatted data.
- Ensure there is a reliable connection between the SMS application and the database to facilitate seamless data exchange.

### Testing

#### Initial Tests

- Conduct initial tests by sending messages that start with "gen" to the shared shortcode.
- Confirm that the application processes these messages correctly.

#### Database Verification

- Check the database to ensure that JSON formatted data sent from the application is correctly received and stored.

#### API Tests

- Test the integration with Africa's Talking API to verify that SMS sending and receiving functionalities work as expected.

### Common Problems and Bugs

- **Message Formatting Issues**: Messages must start with "gen" to be processed correctly. Ensure compliance with this format.
- **API Integration Errors**: If encountering issues, review the Africa's Talking API credentials and integration settings.
- **Database Connection Problems**: Confirm that the database is properly configured to receive JSON data and that there are no issues with connectivity.

To start using the SMS application, follow these steps:

### Send SMS:

- Use the shared shortcode to send a message. (Shortcode = 15054)
- First send the trigger word, “gen” to start the flow.
- Begin each message with the keyword "gen".
- Example: `gen 1`

### Receive Response:

- The application will process the message and send an appropriate response.

### Contributing

**Contact**
For inquiries, contact [Musama, Irene](mailto:irenemwita24@gmail.com).
