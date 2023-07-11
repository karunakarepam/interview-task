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
pytest test_server.py --html=report.html (to run tests with html report)
pytest -s test_server.py (For printing test results on to the console)

**## Performance Test using locust**
To set up the performance testing tool using Locust, you can follow these steps:

Install Locust:

Open your terminal or command prompt.
Ensure that your virtual environment is activated (if you're using one).
Run the command pip install locust to install Locust.
Create a Locust file:

Create a new Python file, e.g., locustfile.py, where you will define your performance test scenarios.
Import the necessary modules: locust and http.client.
Define a class that inherits from locust.HttpUser.
Within the class, define tasks as methods that will simulate requests to your server's endpoints.
Configure the Locust file:

Inside the task methods, use the self.client.get() method to send GET requests to your server's endpoints.
Customize the requests as needed, including any headers, query parameters, or payload data.
You can also include additional logic, such as extracting response data or validating responses.
Start the Locust load test:

Open your terminal or command prompt.
Navigate to the directory where the Locust file (locustfile.py) is located.
Run the command locust --host=http://localhost:5000 to start the Locust web interface.
Replace http://localhost:5000 with the URL of your server.
Configure the number of users and hatch rate:

Access the Locust web interface by opening a web browser and visiting http://localhost:8089.
Specify the number of users to simulate and the hatch rate (the number of users to spawn per second).
Define other relevant options, such as the duration of the test or the stopping criteria.
Start the load test:

Click on the "Start Swarming" button in the Locust web interface.
Locust will start simulating the specified number of users, sending requests to your server's endpoints based on the defined tasks.
Monitor and analyze the results:

Monitor the requests being sent and the response times in the Locust web interface.
Locust provides real-time statistics, graphs, and charts to visualize the performance test results.
Analyze the response times, request rates, and other relevant metrics to assess the performance of your server.
Stop the load test:

Once the load test is complete or when you want to stop it, click on the "Stop" button in the Locust web interface.
Locust will stop sending requests, and you can review the final test results.
Locust offers many features and options to customize your load tests, including the ability to distribute the load across multiple machines. You can refer to the Locust documentation for more detailed instructions on how to set up and configure your performance tests using Locust.

