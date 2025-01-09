**Name:** UMA MAHESHWAR REDDY YATHAM

**Company:** CODTECH IT SOLUTIONS

**ID:** CT08EMS

**Domain:** Java programming

**Duration:** DEC 17 TO JAN 17 2025

**Mentor:** N.SANTHOSH

**Overview of the Code:**

The program is a Java application that consumes a public REST API (OpenWeatherMap API) to fetch and display weather data for a given city. Below is a breakdown of its functionality and key components:

**1. API Endpoint:**

The program communicates with the OpenWeatherMap API to fetch weather data.

The base API URL is:

plaintext
Copy code
https://api.openweathermap.org/data/2.5/weather

**2. Key Features:**

HTTP Request Handling

Uses HttpURLConnection to make an HTTP GET request to the API endpoint.
Sends a properly formatted request with the city name, API key, and optional query parameters like units=metric.
JSON Response

The program receives a JSON-formatted response from the API, which includes weather details, temperature, and other information.
Data Parsing

It extracts specific fields (temp, description) from the raw JSON response using simple string operations.

**Example fields parsed:**

temp: The temperature in the specified city.
description: A short description of the weather condition (e.g., "clear sky").

**Error Handling:**

Checks the HTTP response code.
Prints meaningful error messages if the request fails or the API key is invalid.

**3. How the Code Works:**

a) Fetching Data from the API
The fetchWeatherData() method builds the API URL using the city name and API key.
It opens an HTTP connection, sends the GET request, and reads the response into a String.

b) Parsing the JSON Response
The parseWeatherData() method extracts key information (temperature and weather description) from the JSON response using basic string operations.

c) Printing Output
The raw JSON response is printed for debugging.
Parsed and user-friendly weather details (e.g., temperature and description) are displayed.

4. Key Methods
Method	Purpose
fetchWeatherData	Makes an HTTP GET request to the API and retrieves the JSON response.
parseWeatherData	Extracts specific information (e.g., temperature, weather description).
main	The entry point that calls the above methods and handles the program flow.

6. Dependencies
The code uses only standard Java libraries (HttpURLConnection and BufferedReader), making it lightweight and easy to run.

8. Possible Enhancements
Use JSON Parsing Libraries: For better scalability and readability, replace manual string operations with libraries like Jackson or Gson.
User Input: Allow the user to enter the city name instead of hardcoding it.
Better Error Handling: Add handling for malformed responses, missing fields, and connectivity issues.

![Screenshot (76)](https://github.com/user-attachments/assets/851bce55-a654-4a59-b3d4-5fa527f03452)

