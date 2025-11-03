# WeatherApp | PlantSecure

A modern, responsive weather application that provides real-time weather information, 5-day forecasts, air quality index, and hourly weather updates.

![WeatherApp Preview](weather_assets/img/PlantSecure-Long-Coloured.png)

## Features

- 🌡️ **Real-time Weather Data** - Current temperature, weather conditions, and detailed information
- 📅 **5-Day Forecast** - Extended weather predictions with daily breakdowns
- ⏰ **Hourly Forecast** - Hour-by-hour weather updates for the next 8 hours
- 🌬️ **Air Quality Index (AQI)** - Comprehensive air pollution data including PM2.5, PM10, SO2, CO, NO, NO2, NH3, and O3
- 🌅 **Sunrise & Sunset Times** - Daily solar schedule
- 📍 **Location Services** - Automatic location detection or manual city search
- 💧 **Additional Metrics** - Humidity, pressure, visibility, wind speed, and "feels like" temperature
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices

## Demo

🚀 **[View Live Demo](https://benkmsn.github.io/Plantsecure_WeatherWebapp/)**

## Technologies Used

- **HTML5** - Structure and markup
- **CSS3** - Styling with custom properties and responsive design
- **JavaScript (ES6+)** - Application logic and API interactions
- **OpenWeatherMap API** - Weather data provider
- **Moment.js** - Date and time formatting
- **Font Awesome Pro** - Icon library
- **Boxicons** - Additional icons

## Prerequisites

Before you begin, ensure you have:

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An OpenWeatherMap API key (free tier available)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/WeatherApp_Plantsecure.git
cd WeatherApp_Plantsecure
```

### 2. Get Your OpenWeatherMap API Key

1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Navigate to your API keys section
4. Copy your API key

### 3. Configure the API Key

1. Navigate to the `weather_assets` folder
2. Copy `config.example.js` to `config.js`:
   
   **Windows (Command Prompt):**
   ```bash
   copy weather_assets\config.example.js weather_assets\config.js
   ```
   
   **Windows (PowerShell):**
   ```bash
   Copy-Item weather_assets\config.example.js weather_assets\config.js
   ```
   
   **Mac/Linux:**
   ```bash
   cp weather_assets/config.example.js weather_assets/config.js
   ```

3. Open `weather_assets/config.js` and replace `YOUR_API_KEY_HERE` with your actual API key:
   ```javascript
   const config = {
       apiKey: 'your_actual_api_key_here'
   };
   ```

### 4. Run the Application

**Option A: Using a Local Server (Recommended)**

Using Python 3:
```bash
python -m http.server 8000
```

Using Node.js (with `http-server`):
```bash
npx http-server -p 8000
```

Using VS Code Live Server:
- Install the "Live Server" extension
- Right-click on `index.html` and select "Open with Live Server"

**Option B: Direct File Access**

Simply open `index.html` in your web browser. Note: Some features may not work due to CORS restrictions.

### 5. Access the Application

Open your browser and navigate to:
```
http://localhost:8000
```

## Usage

### Search for a City
1. Type a city name in the search box
2. Click the "Search" button or press Enter
3. View the weather information for that location

### Use Current Location
1. Click the "Current Location" button
2. Allow location access when prompted by your browser
3. View weather information for your current location

## Project Structure

```
WeatherApp_Plantsecure/
├── index.html                          # Main HTML file
├── weather_assets/
│   ├── script.js                       # Main JavaScript application logic
│   ├── style.css                       # Stylesheet
│   ├── config.js                       # API key configuration (not in repo)
│   ├── config.example.js               # Template for config.js
│   └── img/
│       ├── favicon.png                 # Favicon
│       └── PlantSecure-Long-Coloured.png # Logo
├── FontAwesome-pro-master/             # Font Awesome Pro files
│   ├── assets/
│   │   ├── css/
│   │   ├── js/
│   │   └── webfonts/
│   └── README.md
├── .gitignore                          # Git ignore file
├── LICENSE                             # MIT License
└── README.md                           # This file
```

## API Reference

This application uses the following OpenWeatherMap API endpoints:

- **Current Weather Data**: `/data/2.5/weather`
- **5-Day Forecast**: `/data/2.5/forecast`
- **Air Pollution**: `/data/2.5/air_pollution`
- **Geocoding**: `/geo/1.0/direct`
- **Reverse Geocoding**: `/geo/1.0/reverse`

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## Responsive Breakpoints

- Desktop: 1100px and above
- Tablet: 660px - 1099px
- Mobile: 320px - 659px

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## Security Notes

- **Never commit your API key** to the repository
- The `config.js` file is ignored by Git to prevent accidental exposure
- Always use `config.example.js` as a template for other developers
- Consider using environment variables for production deployments

## Troubleshooting

### API Key Issues
- Ensure your API key is active (can take a few hours after creation)
- Verify the API key is correctly placed in `config.js`
- Check the browser console for error messages

### Location Services
- Ensure your browser has permission to access your location
- Check if location services are enabled on your device
- Try using the search feature if location detection fails

### CORS Errors
- Use a local server instead of opening the file directly
- Check if your API key has the correct permissions

### Icons Not Displaying
- Ensure Font Awesome files are in the correct directory structure
- Check browser console for 404 errors on font files
- Verify the paths in `index.html` match your file structure

## Font Awesome Pro License

This project includes Font Awesome Pro. Please note:
- Font Awesome Pro is a commercial product
- The included Font Awesome Pro files are subject to their licensing terms
- If you fork this project, ensure you comply with Font Awesome's license agreement
- Free alternatives: You can replace Font Awesome Pro with Font Awesome Free or other icon libraries

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Weather data provided by [OpenWeatherMap](https://openweathermap.org/)
- Icons by [Font Awesome](https://fontawesome.com/) and [Boxicons](https://boxicons.com/)
- Date formatting by [Moment.js](https://momentjs.com/)

## Contact

For questions or support, please open an issue on GitHub.

---

**Made with ❤️ by BenK**