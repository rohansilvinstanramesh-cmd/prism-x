# PrismX Business Intelligence Platform

A modern, high-performance MERN-stack application serving as a comprehensive Business Intelligence dashboard with advanced analytics, geospatial mapping, and external AI features.

## 🚀 Technologies Used

### Frontend (Client)
- **React 19**: Core library for building a dynamic, component-based user interface.
- **Tailwind CSS & Radix UI**: Utility-first CSS combined with unstyled, accessible primitives for a premium, responsive design.
- **Recharts**: For rendering robust, interactive data visualization charts.
- **React Leaflet**: For interactive geospatial mapping.

### Backend (Server)
- **Node.js + Express**: Scalable backend API server.
- **MongoDB + Mongoose**: Document database handling users, analytics, sales data, and forecasts.
- **JWT Authentication**: Secure user login and route protection.
- **Data Export Tools**: Integration with PDFKit, ExcelJS, and CSV Writer for comprehensive reporting.

### External Services
- **Auxiliary Service Framework**: An external microservice (located in the `service` directory) integrated to provide extended computational and processing features for the platform.
- **OpenAI Integration**: For AI-driven insights and advisory features.

## 📂 Project Structure

```bash
prism-x/
├── client/             # Frontend source files (React)
│   ├── src/
│   │   ├── components/ # Reusable UI components (Sidebar, Charts, Maps)
│   │   ├── pages/      # Main views (Dashboard, Analytics, Sales, Forecast)
│   │   ├── context/    # Global state management
│   │   └── utils/      # API configurations
│   ├── package.json    # Client dependencies
│   └── tailwind.config.js
├── server/             # Backend source files (Node/Express)
│   ├── controllers/    # Request handling logic
│   ├── models/         # Mongoose schemas (User, Sale, Target, Notification)
│   ├── routes/         # Express API endpoints
│   ├── utils/          # Helper functions and Seed Data
│   └── server.js       # Main backend entry point
└── service/            # External microservice for added features
```

## ✨ Key Features
- **Comprehensive Dashboard**: Real-time overview of business metrics and KPIs.
- **Data Visualization**: Rich interactive charts for sales tracking, customer segmentation, and performance forecasting.
- **Geospatial Mapping**: View geographical distribution of targets and sales through integrated maps.
- **AI Advisor**: Integrated AI capabilities providing smart business insights and anomaly detection.
- **Data Export capabilities**: Instantly generate and download reports in PDF, Excel, and CSV formats.

## 🛠️ Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/rohansilvinstanramesh-cmd/prism-x.git
cd prism-x
```

### 2. Setup Database & Backend (`server`)
1. Navigate to the server directory:
   ```bash
   cd server
   npm install
   ```
2. Create a `.env` file in the `server` folder:
   ```env
   # server/.env
   MONGO_URL=your_mongodb_connection_string
   PORT=8001
   JWT_SECRET=your_jwt_secret
   ```
3. Start the backend server:
   ```bash
   npm run dev
   ```

### 3. Setup Frontend (`client`)
1. Open a new terminal and navigate to the client directory:
   ```bash
   cd client
   npm install --legacy-peer-deps
   ```
2. Start the development server:
   ```bash
   npm run start
   ```
   The application will be available at `http://localhost:3000`.

### 4. Setup External Service (`service`)
1. Open a new terminal and navigate to the service directory:
   ```bash
   cd service
   # Install framework dependencies
   pip install -r requirements.txt
   # Run the auxiliary service
   uvicorn server:app --reload --port 8000
   ```

## 🔒 Security Note
Environment variables (`.env`) containing API keys, JWT secrets, and Database URLs are explicitly ignored by Git to prevent exposing credentials. Always ensure you have local `.env` files correctly configured in your `client`, `server`, and `service` directories before running the application.
