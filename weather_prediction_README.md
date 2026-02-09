# Weather Prediction Model

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green.svg)
![Docker](https://img.shields.io/badge/docker-latest-blue.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

FastAPI-based machine learning service for weather prediction, containerized with Docker and deployed via Google Artifact Registry. The system generates weather forecasts using historical local weather data with efficient API performance and scalable deployment.

## Features
- 📊 Historical weather data analysis
- 🌡️ Temperature forecasting with visualization
- 🚀 RESTful API built with FastAPI
- 🐳 Docker containerization for easy deployment
- ☁️ GCP deployment-ready architecture

## Technologies
- **Python 3.9+**
- **FastAPI** - Modern, high-performance web framework
- **TensorFlow** - Machine learning model development
- **Pandas & NumPy** - Data processing and analysis
- **Matplotlib** - Data visualization
- **Docker** - Containerization
- **Google Cloud Platform** - Artifact Registry deployment

## Installation

### Local Setup
```bash
# Clone repository
git clone https://github.com/Timothy-Logan/Weather-Prediction-Model-
cd Weather-Prediction-Model-

# Install dependencies
pip install -r requirements.txt

# Run the application
uvicorn main:app --reload
```

### Docker Setup
```bash
# Build image
docker build -t weather-prediction .

# Run container
docker run -p 8000:8000 weather-prediction
```

## API Documentation

Timothy Logan Assignment #2 - Systems Design Description: This project is a FastAPI application that is intended to be used for weather forcasting. It allows users to upload historical weather data for a specific area, both in text form or just uploading a file to the program, and have future forcasts based off this information. The data and future predictions can also then be visualized into graphs for the user to see. This API could be used both for meteorologist as a tool to relay weather information, whether that be through an app or a website using this API.

### Weather Forecast

![Weather Forecast Graph](https://raw.githubusercontent.com/Timothy-Logan/Weather-Prediction-Model-/main/example_graph.png)

*Example of a graph created on the FastAPI local host.*

### Endpoints

The FastAPI /docs endpoint provides four different items on the endpoint list. These items include:

- **/read root** - Check that it's running on the correct port (I was having issues with this during the assignment)
- **/forecast** - Used to take each of the uploaded files and then do forecasting on said information. Example output: `{"lagged_values": [15.2, 16.8, 14.1], "location": "Ajax, Ontario"}`
- **/forecast/plot** - Plots the data that it's given (the graph above comes from that endpoint)
- **/upload** - Used for the uploading of the files of data

## Model Details

The prediction model uses historical temperature data to forecast future weather patterns. The system analyzes trends and patterns in the data to generate accurate predictions with visualization support.

**Key Features**:
- Time-series analysis of temperature data
- Visualization of predicted vs. actual temperatures
- Support for multiple data formats (CSV uploads, text input)
- RESTful API for easy integration

## Dataset Format

The application expects CSV files with the following structure:
```csv
date,temperature,location
2024-01-01,16.5,Ajax Ontario
2024-01-02,17.0,Ajax Ontario
```

## Future Improvements
- [ ] Add support for additional weather metrics (humidity, precipitation)
- [ ] Implement multiple ML models for comparison
- [ ] Add weather alert notifications
- [ ] Expand to support multiple locations simultaneously
- [ ] Include historical accuracy metrics

## Deployment

This project is configured for deployment to Google Cloud Platform using Google Artifact Registry. The Docker container can be pushed to GAR and deployed using Cloud Run or other GCP services.

## License
MIT License

## Contact
Timothy Logan - [tjlogan9@gmail.com](mailto:tjlogan9@gmail.com)  
GitHub: [@Timothy-Logan](https://github.com/Timothy-Logan)
