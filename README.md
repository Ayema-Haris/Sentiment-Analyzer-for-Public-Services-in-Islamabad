# Islamabad Sentiment Analysis

**Islamabad Sentiment Analysis** is a mobile application that leverages machine learning and natural language processing to analyze and visualize public sentiment based on Google reviews for key services across Islamabad—such as hospitals, malls, restaurants, and public transportation.

---

## 🔍 Features

- Real-time sentiment analysis of Google reviews
- Logistic Regression model trained on annotated data
- Map view with color-coded sentiment markers (positive, neutral, negative)
- Category-wise dashboards with boxplots and trend graphs
- Dynamic filtering by category and location
- FastAPI backend for real-time predictions
- Flutter app with responsive UI 

---

## 🛠️ Technologies Used

| Technology        | Purpose                                   |
|-------------------|-------------------------------------------|
| Flutter + Dart    | Cross-platform mobile development         |
| Python + FastAPI  | Backend for data scraping & analysis      |
| Google Places API | Collects reviews and metadata             |
| TF-IDF + Scikit-learn | Text vectorization & sentiment model   |
| Google Maps API   | Geolocation and map visualization         |
| Recharts          | Data visualization in dashboard           |

---

# Project Setup Instructions

## Step 1: Clone the GitHub Repository
Open your terminal and run the following command to clone the repository:

```bash
git clone https://github.com/Ayema-Haris/Sentiment-Analyzer-for-Public-Services-in-Islamabad.git
```

## Step 2: Set Up and Run the Backend
1. Navigate to the Sentiment-Analyzer-for-Public-Services-in-Islamabad root folder where backend and frontend both exist
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```
4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Step 3: Start the Backend Server
5. Navigate to the backend folder from the root Sentiment-Analyzer-for-Public-Services-in-Islamabad folder 
```bash
cd backend
```
6. Then from the backend folder run this command

```bash
python main.py
```

## Step 4: Get Your Local IP Address
Run the following command in your terminal to get your local IPv4 address:

- On Windows:
  ```bash
  ipconfig
  ```
- On macOS/Linux:
  ```bash
  ifconfig
  ```

Note your **IPv4 address** — you'll need it for the frontend configuration.

## Step 5: Configure and Run the Frontend
1. Leave the backend terminal running and create a new terminal then navigate to the `frontend` folder using the cd command:
   ```bash
   cd frontend
   ```
2. Run:
   ```bash
   flutter pub get
   ```
3. Go to:
   
   lib/screens/api_service.dart
   
4. Replace the base URL with your own IP address (keep the port `8000` as is).  
   Example:
   ```dart
   const String baseUrl = "http://x.x.x.x:8000";
   ```

---

## 🚨 Notes:
- **Google Maps** will only work if:
  - You use your **own Google Maps API key**.
  - You run the app **on a mobile device**, not a laptop/emulator.

### To update the API key:
1. Go to:
   ```
   frontend/android/app/src/main/AndroidManifest.xml
   ```
2. Replace the placeholder API key with your own:
   ```xml
   <meta-data android:name="com.google.android.geo.API_KEY"
              android:value="YOUR_API_KEY_HERE"/>
   ```

---

## 🤖 Contribution

Pull requests are welcome!
