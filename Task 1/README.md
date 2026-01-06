## Instructions for Pulling the Data

1. Install Docker on your machine.

2. Pull the image from Docker Hub:
   [Image URL](https://hub.docker.com/r/femiml/zenquotes)

3. Create a .env file with required environment variables: e.g
   DB_HOST=db
   DB_NAME=DB_NAME
   DB_USER=USERNAME
   DB_PASSWORD=PASSWORD
   SMTP_USER=your_email
   SMTP_PASS=your_password
   ...

4. Start the service with Docker Compose:
   docker compose up

   This will start:
   - The Python quote-delivery service
   - A Postgres database container

5. Check logs to ensure:
   - Quotes are fetched from ZenQuotes API
   - Database connection succeeds
   - Emails are sent successfully
