# Interview Portal

A comprehensive interview management system built with FastAPI backend and React frontend for conducting automated interviews.

## Documentation Links

- [Backend Documentation](./backend/README.md)
- [Frontend Documentation](./frontend/README.md)

## Tech Stack

### Backend
- FastAPI
- MySQL
- SQLAlchemy
- JWT Authentication
- Python 3.8+

### Frontend
- React 18
- TypeScript
- Redux Toolkit
- Tailwind CSS
- Vite
- React Router DOM
- React Query

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Node.js 14 or higher
- MySQL 8.0+
- Git

### Setting Up Backend

1. Navigate to backend directory:

```bash
cd backend
```

2. Create and activate virtual environment:

```bash
# For Windows
python -m venv .venv
.venv\Scripts\activate

# For Linux/Mac
python3 -m venv .venv
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Configure environment variables:

```bash
# Copy example env file
cp .env.example .env

# Update the .env file with your MySQL credentials:
DATABASE_URL=mysql+pymysql://root:password@localhost/interview_portal
SECRET_KEY=your-super-secret-key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

5. Start the backend server:

```bash
uvicorn app.main:app --reload
```

The backend server will start at `http://localhost:8000`

- API Documentation: `http://localhost:8000/docs`
- Alternative Documentation: `http://localhost:8000/redoc`

### Setting Up Frontend

1. Navigate to frontend directory:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

The frontend application will be available at `http://localhost:5173`

## Features

- User Authentication with JWT
- Role-based Access Control:
  - HR
  - Interviewer 
  - Evaluator
  - Candidate
- Candidate Registration and Photo Verification
- Interview Scheduling and Management
- Real-time Interview Proctoring
- Interview Questions Management
- Candidate Progress Tracking
- File Upload Management
- Resume Parsing

## Project Structure

```
interview-portal/
├── backend/               # FastAPI backend
│   ├── app/              # Application code
│   │   ├── main.py      # FastAPI application
│   │   ├── database.py  # Database configuration
│   │   ├── models/      # SQLAlchemy models
│   │   ├── routers/     # API routes
│   │   ├── schemas/     # Pydantic schemas
│   │   └── security.py  # Authentication logic
│   ├── requirements.txt  # Python dependencies
│   └── README.md        # Backend documentation
│
└── frontend/            # React frontend
    ├── src/            # Source code
    │   ├── components/ # React components
    │   ├── pages/      # Page components
    │   ├── store/      # Redux store
    │   ├── services/   # API services
    │   └── main.tsx    # Entry point
    ├── package.json    # Node.js dependencies
    └── README.md       # Frontend documentation
```

## Development Workflow

1. Start the backend server:
```bash
cd backend
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
uvicorn app.main:app --reload
```

2. Start the frontend development server:
```bash
cd frontend
npm run dev
```

3. Access the application:
- Frontend: `http://localhost:5173`
- API Documentation: `http://localhost:8000/docs`

## Database Setup

1. Create MySQL database:
```sql
CREATE DATABASE interview_portal;
```

2. Run migrations:
```bash
cd backend
mysql -u root -p interview_portal < DB_Structure.sql
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## License

This project is licensed under the MIT License.

## Support

If you encounter any issues or have questions:
1. Check the [Backend Documentation](./backend/README.md)
2. Check the [Frontend Documentation](./frontend/README.md)
3. Open an issue in the repository

## Authors

- Backend Team - FastAPI Implementation
- Frontend Team - React Implementation
