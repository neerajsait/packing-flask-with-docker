                                                                 Flask Date-Time API in Docker
This is a simple Flask application that displays the current date and time. The application is
containerized using Docker.
Features:
- Displays the current date and time
- Runs inside a Docker container
- Uses Python Flask for the backend
- Supports custom time zones (if pytz is installed)
Prerequisites:
Ensure you have the following installed:
- Python 3.9+ (https://www.python.org/)
- Docker (https://www.docker.com/get-started)
Setup & Installation:
Clone this repository:
git clone https://github.com/your-repo/date-time-flask-docker.git
cd date-time-flask-docker
Install dependencies (Optional for local testing):
pip install -r requirements.txt
Dockerfile:
FROM python:3.9
WORKDIR /app
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 5000
CMD ["python", "app.py"]
Docker Commands:
# Navigate to your project directory
cd "D:\python project\datetime"
# Step 1: Build the Docker image
docker build -t date-time .
# Step 2: Run the Docker container
docker run -d -p 5000:5000 date-time
# Step 3: Verify that the container is running
docker ps
# Step 4: Check logs (if needed)
docker logs <container_id>
# Step 5: Stop the running container (if needed)
docker stop <container_id>
# Step 6: Remove the container (if needed)
docker rm <container_id>
# Step 7: Remove the Docker image (if needed)
docker rmi date-time
# Step 8: Rebuild and restart (if changes are made)
docker build -t date-time .
docker run -d -p 5000:5000 date-time
# Step 9: Open the application in the browser
http://localhost:5000
