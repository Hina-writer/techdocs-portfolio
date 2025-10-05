# Weather Forecast API Documentation

## Introduction

This documentation helps developers interact with the **Open Weather API** to access real-time and forecasted weather data for locations worldwide. The API provides multiple endpoints, including:

- **Current Weather Data**: Retrieve up-to-date weather information for a given location.
- **5-Day Forecast**: Access short-term weather predictions at 3-hour intervals for informed decision-making.

This guide focuses on these two endpoints to help you get started quickly and confidently.

---

## Base URL

*https://api.openweathermap.org/data/2.5/*


---

## Authentication

To use the Weather API, you need an API key. Sign up at OpenWeather to get yours.  
Include the API key as a query parameter in every request.  

**Example:**


Replace `{city name}` and `{YOUR_API_KEY}` with actual values.

---

## Endpoints

### 1. Current Weather Data

- **Endpoint URL:** `/weather`  
- **Method:** GET  

**Query Parameters:**

| Parameter | Type   | Required | Description       |
|-----------|--------|----------|-------------------|
| `q`       | string | Yes      | City name (e.g., London) |
| `appid`   | string | Yes      | Your API key       |

**Example Request:**

*https://api.openweathermap.org/data/2.5/weather?q=New%20York&appid={YOUR_API_KEY}*


**Response Example:**

```json
{
  "weather": [
    {
      "description": "clear sky",       // Weather condition description
      "icon": "01d"                     // Icon code for displaying weather image
    }
  ],
  "main": {
    "temp": 295.15,                    // Temperature in Kelvin
    "pressure": 1013,                  // Atmospheric pressure (hPa)
    "humidity": 53                    // Humidity (%)
  },
  "name": "New York"                  // Location name
}
```
## 5-Day Forecast

Retrieve weather forecast data for the next 5 days at 3-hour intervals.

**Endpoint URL:** `/forecast`  
**Method:** `GET`

### Query Parameters

| Parameter | Type   | Required | Description               |
|-----------|--------|----------|---------------------------|
| `q`       | string | Yes      | City name (e.g., Paris)   |
| `appid`   | string | Yes      | Your API key              |

**Example Request:**

*https://api.openweathermap.org/data/2.5/forecast?q=Paris&appid={YOUR_API_KEY}*

**Response Example:**
```json
{
  "city": {
    "name": "Paris",
    "country": "FR"
  },
  "list": [
    {
      "dt_txt": "2025-10-05 12:00:00",
      "main": {
        "temp": 289.92,
        "humidity": 82
      },
      "weather": [
        {
          "description": "light rain",
          "icon": "10d"
        }
      ],
      "wind": {
        "speed": 4.1
      }
    }
    // ...more 3-hour intervals
  ]
}
```

## Error Codes

The API uses standard HTTP status codes to indicate success or failure:

| Status Code | Meaning               | Description                                      |
|-------------|-----------------------|--------------------------------------------------|
| `200`       | OK                    | The request was successful.                      |
| `401`       | Unauthorized          | The API key is missing or invalid.               |
| `404`       | Not Found             | The requested resource could not be found.       |
| `500`       | Internal Server Error | Something went wrong on the server side.         |

---
## Resources

- [OpenWeather API Documentation](https://openweathermap.org/api)
- [Sign Up for an API Key](https://home.openweathermap.org/users/sign_up)
- [API Status & Limits](https://openweathermap.org/appid)
