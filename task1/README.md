# Hello from xops!! - Nginx Docker Example

This project demonstrates how to serve a simple HTML page using Nginx in a Docker container.

## Files

- `index.html` — The HTML file with a nice UI greeting from xops.
- `Dockerfile` — Docker configuration to run Nginx and serve the HTML page.

## How to Build and Run

1. **Build the Docker image:**
   ```
   docker build -t xops-nginx .
   ```

2. **Run the Docker container:**
   ```
   docker run -d -p 8080:80 xops-nginx
   ```

3. **View in browser:**
   Open [http://localhost:8080](http://localhost:8080) to see the page.

## Requirements

- [Docker](https://www.docker.com/) installed on your system.

##