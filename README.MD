# Movie App Server

This Node.js server, built using Express, serves as the backend for a movie app. It interacts with a PostgreSQL database using the 'pg' library and handles CRUD operations for movie data. The server is equipped with CORS middleware to allow cross-origin resource sharing and uses environment variables for configuration, including the database connection string.

## Endpoints

- **GET '/'** - Returns a simple "hello world" message.
- **GET '/api/movies'** - Retrieves a list of all movies from the database.
- **GET '/api/movies/:id'** - Retrieves details of a specific movie based on its ID.
- **POST '/api/movies'** - Adds a new movie to the database after validating the required fields.
- **PUT '/api/movies/:id'** - Updates details of a specific movie based on its ID.
- **DELETE '/api/movies/:id'** - Deletes a specific movie based on its ID.

## Middleware

- Global middleware logs incoming requests, showing the HTTP method and path.

## Validation

- Includes a middleware 'validateMovie' to ensure that required fields are present when adding a new movie.

## Error Handling

- Catches errors and returns appropriate HTTP responses with error messages.
- Uses a generic error middleware to handle validation errors and responds with a 400 status code.

## Environment

- Utilizes environment variables for configuration, such as the port number and the PostgreSQL connection string.

## Port

The server listens on the specified port (either from the environment variable or defaulting to 8000) and logs a message once it's running.
