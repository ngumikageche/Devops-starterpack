# Flask App Deployment with Gunicorn and Nginx on Ubuntu 22.04

This script automates the process of setting up a Flask web application to run with **Gunicorn** and be served via **Nginx** on **Ubuntu 22.04**.

## Prerequisites

- Ubuntu 22.04 or later
- A domain name or public IP address (for Nginx configuration)
- A Flask app repository (or local Flask app directory)

## What the Script Does

This script performs the following tasks:

1. **System Update & Package Installation:**
   - Updates the system and installs required dependencies (`python3`, `pip`, `virtualenv`, `nginx`, etc.).
   
2. **Flask App Setup:**
   - Clones a Flask app from a Git repository (you can modify this section for your app).
   - Creates a virtual environment for the app and installs dependencies from `requirements.txt`.
   
3. **Gunicorn Setup:**
   - Installs Gunicorn and sets it up as a system service.
   - Configures Gunicorn to run your Flask app with 3 worker processes.

4. **Nginx Configuration:**
   - Configures Nginx to reverse proxy requests to Gunicorn through a Unix socket.
   - Sets up Nginx to listen on port 80 for HTTP requests.
   
5. **Firewall Configuration:**
   - Configures `ufw` to allow traffic on ports 80 and 443 (HTTP and HTTPS).

6. **Service Management:**
   - Starts Gunicorn and Nginx services and enables them to start on boot.









