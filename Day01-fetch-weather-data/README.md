# Weather Dashboard GCP

This project fetches weather data from the OpenWeather API and saves it to a Google Cloud Storage bucket.

- External API Integration (OpenWeather API)
- Cloud Storage (Google Cloud Storage)
- Infrastructure as Code
- Version Control (Git)
- Python Development
- Error Handling
- Environment Management

## Features

- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in Google Cloud Storage
- Supports multiple cities tracking
- Timestamps all data for historical tracking

## Prerequisites

- Python 3.6+
- Google Cloud SDK
- A Google Cloud project with billing enabled
- OpenWeather API key

## Setup

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/30-days-cloud--devops-engineering.git
    cd 30-days-cloud--devops-engineering/Day01-fetch-weather-data
    ```

2. **Create a virtual environment**:

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:

    Create a `.env` file in the project directory and add your OpenWeather API key and Google Cloud Storage bucket name:

    ```plaintext
    OPENWEATHER_API_KEY=your_openweather_api_key
    GCP_BUCKET_NAME=your_gcp_bucket_name
    ```

5. **Authenticate with Google Cloud**:

    ```bash
    gcloud auth login
    gcloud config set project your-gcp-project-id
    ```

6. **Set up ADC for local development credentials**

    ```bash
    gcloud auth application-default login
    ```

## Usage

Run the script to fetch weather data and save it to the Google Cloud Storage bucket:

```bash
python3 weather_dashboard.py
```

## Project Structure

```plaintext

├── weather_dashboard.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

## Dependencies

- google-cloud-storage
- requests
- python-dotenv