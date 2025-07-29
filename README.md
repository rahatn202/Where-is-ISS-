# Where is the ISS?

This project provides a Python script to determine if the International Space Station (ISS) is currently overhead a user-defined location. It utilizes external APIs to fetch location data and the real-time position of the ISS.

---

## Defining "Overhead"

The ISS orbits Earth at an impressive speed of approximately 17,500 miles per hour, meaning it traverses the sky quickly and remains overhead for only a brief period. To precisely define "overhead" and ensure optimal viewing conditions, we use a **±5° tolerance**. This narrow window provides the most accurate representation of when the ISS is truly overhead, allowing observers to focus on peak visibility moments.

Specifically, the ISS is considered overhead if its latitude and longitude fall within ±5° of the user's position during its brief passage.

Key factors in this definition include:

* **Latitude and Longitude Tolerance:** The ISS must be within ±5° of the user's location, providing a precise range for tracking its fast orbit.
* **Orbital Inclination Check:** This implicitly ensures the ISS is within its orbital bounds of -51.6° to 51.6° latitude, making it physically possible to be overhead.
* **Duration of Overhead:** The ISS's rapid movement is considered within the ±5° tolerance, enabling users to track its position during the brief window when it's genuinely overhead.

**Reference**: [Spot The Station NASA](https://spotthestation.nasa.gov/message_example.cfm#:~:text=It%20represents%20the%20height%20of,will%20be%20about%2010%20degrees.)

---

## Getting Started

### Prerequisites

To run this script, you'll need:

* **Python 3.x**
* **`requests` library**: For making API calls.
* A **Google Maps Geocoding API Key**: This is necessary to convert addresses to latitude and longitude.

### Installation

1.  Clone this repository (or copy the code into a `.py` file).
2.  Install the required Python library:
    ```bash
    pip install requests
    ```

### API Key Setup

Obtain a Google Maps Geocoding API key from the [Google Cloud Console](https://console.cloud.google.com/). Please note that while some Google Cloud services offer a free tier, usage of the Geocoding API might require billing information.

Once you have your API key, replace the placeholder `api_key` in the `main()` function or at the top of the script with your actual key:

```python
api_key = "YOUR_Maps_API_KEY_HERE"
