# STUDIX - Smart Schedule Management App

A modern React + Express + MongoDB application for university students to manage their schedules with AI-powered natural language input.

## Features

- 📅 **Interactive Calendar** - Visual schedule management with drag-and-drop
- 🤖 **AI Chatbot** - Natural language schedule creation ("I have math homework due tomorrow")
- 📊 **Statistics Dashboard** - Track completion rates and productivity
- 🌙 **Dark Mode** - Toggle between light and dark themes
- 📱 **Responsive Design** - Works on mobile, tablet, and desktop
- 🔔 **Smart Notifications** - 1 day before, 15 minutes before, morning of
- 🏷️ **Keyword Extraction** - AI automatically extracts relevant keywords
- ✍️ **Spell Correction** - Auto-corrects typos in natural language input

## Tech Stack

### Frontend
- React 19 with Vite
- Tailwind CSS for styling
- React Router for navigation
- Lucide React for icons
- Date-fns for date manipulation
- React Hook Form + Zod for form validation
- React Hot Toast for notifications

### Backend
- Node.js with Express
- MongoDB with Mongoose
- CORS for cross-origin requests
- Natural language processing for AI features
- Cron jobs for notifications

## Setup Instructions

### Prerequisites
- Node.js (v18+)
- MongoDB (local or cloud)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd studix-app
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   
   # Create .env file with your settings
   cp .env.example .env
   
   # Start MongoDB (if running locally)
   mongod
   
   # Start the backend server
   npm run dev
   ```
   
   The backend will run on `http://localhost:3000`

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   
   # Start the frontend development server
   npm run dev
   ```
   
   The frontend will run on `http://localhost:5173`

### Environment Variables

Create a `.env` file in the backend directory:

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/studix
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
```

## Usage

### Natural Language Schedule Creation

The AI chatbot understands natural language input like:
- "I have a math assignment due tomorrow at 3pm"
- "Meeting with professor on Friday at 10am"
- "Study for chemistry exam next week"
- "Submit project report by Monday"

### Features Demo

1. **Dashboard**: View statistics, upcoming schedules, and quick actions
2. **Calendar**: Interactive monthly view with schedule management
3. **AI Chat**: Natural language schedule creation with follow-up questions
4. **Dark Mode**: Toggle in the header
5. **Responsive**: Test on different screen sizes

## API Endpoints

### Schedules
- `GET /api/schedules` - Get all schedules
- `GET /api/schedules/range?startDate=YYYY-MM-DD&endDate=YYYY-MM-DD` - Get schedules in date range
- `GET /api/schedules/stats` - Get schedule statistics
- `POST /api/schedules` - Create new schedule
- `PUT /api/schedules/:id` - Update schedule
- `PATCH /api/schedules/:id/complete` - Mark schedule as completed
- `DELETE /api/schedules/:id` - Delete schedule

### AI
- `POST /api/ai/parse` - Parse natural language text into schedule data
- `POST /api/ai/correct` - Spell check and correct text

## Performance Requirements (NFR)

- ⚡ **AI Response Time**: < 2 seconds
- 🎯 **Natural Language Accuracy**: 90%+
- 🔧 **Spell Correction**: Automatic typo detection and correction
- 💾 **Data Storage**: Local + MongoDB persistence
- 🛡️ **Error Handling**: Graceful server error management

## Project Structure

```
studix-app/
├── backend/
│   ├── models/          # MongoDB schemas
│   ├── routes/          # API endpoints
│   ├── server.js        # Express server
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── contexts/    # React contexts
│   │   ├── utils/       # API utilities
│   │   └── App.jsx      # Main app component
│   ├── public/
│   └── package.json
└── README.md
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License.

## Troubleshooting

### Common Issues

1. **Backend not starting**: Check if MongoDB is running
2. **Frontend not loading**: Ensure backend is running on port 3000
3. **AI not responding**: Check backend logs for API errors
4. **Styles not loading**: Run `npm install` in frontend directory

### Development Tips

- Use browser dev tools to debug API calls
- Check MongoDB connection in backend logs
- Test responsive design using browser dev tools
- Use React DevTools for component debugging