# Flask App with Nginx Reverse Proxy on AWS EC2

## What it does
A Python Flask app deployed on EC2 with nginx acting as a reverse proxy. Users access port 80 (normal HTTP) and nginx forwards requests to Flask running internally on port 5000.

## Architecture
User → nginx (port 80) → Flask (port 5000) → Response back to user

## Tech Used
- AWS EC2 (Ubuntu)
- Python 3
- Flask
- nginx (reverse proxy)
- Linux

## What I Learned
- How nginx reverse proxy works
- Difference between nginx serving static files vs forwarding to backend
- How to configure proxy_pass in nginx
- Why 127.0.0.1 is used for internal communication
- How production apps hide backend from users

## How to Replicate
1. Launch EC2, open port 80 only
2. Install nginx and Flask
3. Configure /etc/nginx/sites-available/default with proxy_pass
4. Run python3 app.py
5. Visit EC2 public IP in browser — no port number needed

## Project Structure
- `app.py` — Flask application
