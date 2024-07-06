# HomeFinder

HomeFinder is a platform designed to link landlords and tenants in Nairobi. The application provides a user-friendly interface for property listings, advanced search, real-time messaging, and secure transactions.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Architecture](#architecture)
- [Setup](#setup)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Database](#database)
  - [Real-time Communication](#real-time-communication)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- Property Listings
- Advanced Search and Filters
- User Profiles
- Real-time Messaging
- Secure Transactions
- Admin Panel

## Technologies

- **Frontend:** React.js, Context API/Redux, Axios, styled-components
- **Backend:** Django, Django Rest Framework
- **Database:** MySQL
- **Real-time Communication:** Socket.io
- **Deployment:** Docker, Kubernetes, CI/CD tools

## Architecture

### Frontend

- React.js for building user interfaces
- Context API or Redux for state management
- Axios for API calls
- styled-components for styling

### Backend

- Django for backend framework
- Django Rest Framework for building RESTful APIs
- JWT for authentication

### Database

- MySQL for relational database management

### Real-time Communication

- Socket.io for real-time messaging

## Setup

### Frontend

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/homefinder.git
   cd homefinder/frontend```

2. Install dependencies:

   ```sh
   npm install```

3. Start the development server:

   ```sh
   npm start```


### Backend
1. Clone the repository:

   ```sh
git clone https://github.com/yourusername/homefinder.git
cd homefinder/backend```

2. Create a virtual environment and activate it:

   ```sh
   python3 -m venv venv
   source venv/bin/activate```

3. Install dependencies:

   ```sh
   pip install -r requirements.txt```

4. Configure the database in settings.py:

   ```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'keja_finder',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}```

5. Apply migrations:

   ```sh
   python manage.py makemigrations
   python manage.py migrate```

6. Start the development server:

   ```sh
   python manage.py runserver```

###  Database

1. Install MySQL and create a database:
   ```sql
   CREATE DATABASE Homefinder;
   CREATE USER 'your_mysql_user'@'localhost' IDENTIFIED BY 'your_mysql_password';
   GRANT ALL PRIVILEGES ON keja_finder.* TO 'your_mysql_user'@'localhost';
   FLUSH PRIVILEGES;```

### Real-time Communication

1. Install dependencies for Socket.io in the backend or a separate Node.js service.

Example setup (Node.js):

```sh
npm install socket.io```

Integration example:

```javascript
const io = require('socket.io')(server);

io.on('connection', (socket) => {
    console.log('A user connected');

    socket.on('sendMessage', (message) => {
        io.emit('receiveMessage', message);
    });

    socket.on('disconnect', () => {
        console.log('User disconnected');
    });
});```

### Contributing
Contributions are welcome! Please create an issue or submit a pull request for any changes.

### License
This project is licensed under the MIT License.


Feel free to modify any part of this `README.md` to better suit your 

