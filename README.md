# xmProjectInterviewTask
# Fake HTTP Server

This project provides a fake HTTP server written in Python using Flask. The server simulates the behavior of an API similar to https://swapi.dev/. It supports three endpoints: `/people/<id>/`, `/planets/<id>/`, and `/starships/<id>/`.

## Getting Started

To set up and run the fake HTTP server, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/fake-http-server.git`
2. Navigate to the project directory: `cd fake-http-server`
3. Set up a virtual environment (optional): `python -m venv env`
4. Activate the virtual environment: `source env/bin/activate` (Unix) or `.\env\Scripts\activate` (Windows)
5. Install the dependencies: `pip install -r requirements.txt`
6. Start the server: `python server.py`
7. The server will be running at http://localhost:5000

## Automated Test Suite

The project includes an automated test suite using pytest and the requests module to verify the expected behavior of the server's endpoints. To run the tests, use the following command:

