# Flask Armstrong Number API

This is a simple Flask-based API that checks whether a given number is an **Armstrong number**. An Armstrong number (also known as a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.

## Features
- A root endpoint (`/`) that returns a simple **Hello, World!** message.
- An endpoint (`/armstrong/<int:n>`) that checks if `n` is an Armstrong number.
- Returns a JSON response containing the number and whether it is an Armstrong number.

## Prerequisites
Make sure you have **Python** installed on your system. You also need to install **Flask** if you haven't already:

```bash
pip install flask
```

## How to Run the Application
1. Clone this repository or copy the script.
2. Navigate to the project directory.
3. Run the following command:
   ```bash
   python app.py
   ```
4. The application will start on `http://127.0.0.1:5000/`

## Usage
### 1. Test Root Endpoint
Open your browser or use `curl`:
```bash
curl http://127.0.0.1:5000/
```
#### Response:
```
Hello, World!
```

### 2. Check Armstrong Number
Pass an integer value in the URL to check if it's an Armstrong number:
```bash
curl http://127.0.0.1:5000/armstrong/153
```
#### Response (For Armstrong Number):
```json
{
    "Number": 153,
    "Armstrong": true,
    "Server IP": "122.34.66475.7"
}
```

#### Response (For Non-Armstrong Number):
```json
{
    "Number": 123,
    "Armstrong": false,
    "Server IP": "122.34.66475.7"
}
```

## Potential Improvements
- Add error handling for invalid inputs.
- Remove hardcoded "Server IP" and dynamically fetch it.
- Enhance UI by integrating with a frontend framework.

## License
This project is licensed under the MIT License.

