# 💰 Budget Finance Tracker

A free, open-source personal finance and budgeting app built with React, Node.js, and SQLite. Track expenses, manage budgets, and visualize your financial health with an intuitive interface.

## ✨ Features

- 👤 **User Authentication** - Secure login and signup
- 💼 **Budget Management** - Create, update, and track budgets by category
- 💸 **Expense Tracking** - Log daily expenses with categories
- 📈 **Income Management** - Track income sources
- 📊 **Dashboard & Analytics** - Visual charts and reports
- 🏷️ **Category Management** - Organize expenses by custom categories
- 📥 **Data Export** - Export reports as CSV/JSON
- 🔒 **Privacy First** - Your data stays on your device (local SQLite)
- 📱 **Responsive Design** - Works on desktop and tablet

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, TypeScript, Vite, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | SQLite3 |
| **Charts** | Recharts |
| **Authentication** | JWT tokens |
| **API** | RESTful |

## 📋 Prerequisites

Before you begin, ensure you have installed:
- **Node.js** v18.0.0 or higher ([Download](https://nodejs.org/))
- **npm** v9.0.0 or higher (comes with Node.js)
- **Git** ([Download](https://git-scm.com/))

## 🚀 Quick Start

### 1. Clone the Repository
\`\`\`bash
git clone https://github.com/mpaz01-code/budget-finance-tracker.git
cd budget-finance-tracker
\`\`\`

### 2. Setup Backend
\`\`\`bash
cd backend
npm install
cp .env.example .env
npm start
\`\`\`

The backend will run on \`http://localhost:5000\`

### 3. Setup Frontend (in a new terminal)
\`\`\`bash
cd frontend
npm install
npm run dev
\`\`\`

The frontend will run on \`http://localhost:5173\`

### 4. Open Your Browser
Navigate to \`http://localhost:5173\` and start budgeting!

## 📁 Project Structure

\`\`\`
budget-finance-tracker/
├── backend/
│   ├── src/
│   │   ├── models/          # Database schemas & queries
│   │   ├── routes/          # API endpoint routes
│   │   ├── controllers/     # Business logic
│   │   ├── middleware/      # Authentication & validation
│   │   ├── db.js            # SQLite database setup
│   │   └── server.js        # Express server config
│   ├── package.json
│   ├── .env.example
│   └── tsconfig.json
│
├── frontend/
│   ├── src/
│   │   ├── components/      # Reusable React components
│   │   ├── pages/           # Full page components
│   │   ├── services/        # API service calls
│   │   ├── hooks/           # Custom React hooks
│   │   ├── styles/          # Global styles
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── public/
│   ├── package.json
│   ├── vite.config.ts
│   └── tsconfig.json
│
├── docker-compose.yml       # Docker setup for easy deployment
├── .gitignore
└── README.md
\`\`\`

## 🔧 Environment Variables

### Backend (.env)
\`\`\`
PORT=5000
NODE_ENV=development
DATABASE_PATH=./data/budget.db
JWT_SECRET=your-secret-key-change-this
JWT_EXPIRE=7d
\`\`\`

### Frontend (.env)
\`\`\`
VITE_API_BASE_URL=http://localhost:5000/api
\`\`\`

## 🎯 API Endpoints

### Authentication
- \`POST /api/auth/register\` - Register new user
- \`POST /api/auth/login\` - Login user
- \`POST /api/auth/logout\` - Logout user

### Budgets
- \`GET /api/budgets\` - Get all budgets
- \`POST /api/budgets\` - Create new budget
- \`PUT /api/budgets/:id\` - Update budget
- \`DELETE /api/budgets/:id\` - Delete budget

### Expenses
- \`GET /api/expenses\` - Get all expenses
- \`POST /api/expenses\` - Create expense
- \`PUT /api/expenses/:id\` - Update expense
- \`DELETE /api/expenses/:id\` - Delete expense

### Income
- \`GET /api/income\` - Get all income entries
- \`POST /api/income\` - Create income entry
- \`PUT /api/income/:id\` - Update income entry
- \`DELETE /api/income/:id\` - Delete income entry

### Categories
- \`GET /api/categories\` - Get all categories
- \`POST /api/categories\` - Create category
- \`DELETE /api/categories/:id\` - Delete category

### Reports
- \`GET /api/reports/summary\` - Get financial summary
- \`GET /api/reports/expenses-by-category\` - Expense breakdown
- \`GET /api/reports/trends\` - Monthly trends
- \`GET /api/reports/export\` - Export data (CSV/JSON)

## 🤖 Using with AI (Claude/Cursor)

### With Claude (Poe.com or Claude.ai):
1. Copy any code snippet and paste in Claude
2. Ask for explanations, bug fixes, or feature additions
3. Example: *"Explain how the budget calculation works in this code"*
4. Paste Claude's response back into your code

### With Cursor (VS Code replacement):
1. Download [Cursor](https://www.cursor.com/)
2. Open this project folder
3. Press \`Ctrl+K\` (Windows/Linux) or \`Cmd+K\` (Mac) to ask AI
4. Example: *"Add a feature to filter expenses by date range"*
5. Cursor will generate code directly in your editor

### With GitHub Copilot:
1. Use in VS Code or JetBrains IDEs
2. Start typing a comment describing what you need
3. Copilot suggests code completions

## 🐳 Docker Deployment

### Build and Run with Docker
\`\`\`bash
docker-compose up --build
\`\`\`

This will start:
- Backend on \`http://localhost:5000\`
- Frontend on \`http://localhost:3000\`
- SQLite database in a volume

## 🌐 Free Hosting Options

### Frontend Hosting
- **Vercel** (Recommended) - vercel.com - Free tier
- **Netlify** - netlify.com - Free tier
- **GitHub Pages** - Free with GitHub account

### Backend Hosting
- **Render.com** - Free tier (250 hours/month)
- **Railway.app** - $5 free credits/month
- **Fly.io** - Free tier available
- **Heroku** - Limited free tier

### Database Hosting
- **Supabase** - PostgreSQL free tier (can replace SQLite)
- **Railway** - Included in free credits
- **Render** - Free PostgreSQL

## 📚 Learning Resources

- [React Documentation](https://react.dev)
- [Node.js Guide](https://nodejs.org/en/docs)
- [SQLite Tutorial](https://www.sqlite.org/docs.html)
- [Express.js Guide](https://expressjs.com)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)

## 🤝 Contributing

Contributions are welcome! Here's how to help:

1. Fork the repository
2. Create a feature branch (\`git checkout -b feature/amazing-feature\`)
3. Commit changes (\`git commit -m 'Add amazing feature'\`)
4. Push to branch (\`git push origin feature/amazing-feature\`)
5. Open a Pull Request

## 📝 Development Workflow

### Using Claude for Help
\`\`\`
1. Get stuck on a problem
2. Copy the error or code snippet
3. Open Claude (poe.com/Claude or claude.ai)
4. Paste and ask: "Why is this failing?" or "How do I implement this?"
5. Copy the response and implement it
\`\`\`

### Using Cursor for Real-time Help
\`\`\`
1. Open project in Cursor
2. Highlight problematic code
3. Press Cmd+K (Mac) or Ctrl+K (Windows/Linux)
4. Ask your question
5. Cursor suggests or generates code inline
\`\`\`

## 🐛 Troubleshooting

### Port Already in Use
\`\`\`bash
# Windows
netstat -ano | findstr :5000

# macOS/Linux
lsof -i :5000
\`\`\`

### Database Issues
\`\`\`bash
# Delete the database and restart (clears all data)
rm backend/data/budget.db
npm start
\`\`\`

### Dependencies Not Installing
\`\`\`bash
# Clear npm cache and reinstall
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
\`\`\`

## 📄 License

This project is licensed under the MIT License.

## 💡 Future Enhancements

- [ ] Mobile app (React Native)
- [ ] Recurring expenses/income
- [ ] Bill reminders & notifications
- [ ] Multi-currency support
- [ ] Family budget sharing
- [ ] Advanced forecasting
- [ ] Investment tracking
- [ ] Tax reporting

## 🆘 Support

- **Issues**: [Open an issue on GitHub](https://github.com/mpaz01-code/budget-finance-tracker/issues)
- **Discussions**: Start a GitHub discussion
- **Email**: Create an issue and mention it there

## 🙏 Acknowledgments

- Inspired by [Actual Budget](https://actualbudget.org)
- Built with [React](https://react.dev) and [Node.js](https://nodejs.org)
- Styled with [Tailwind CSS](https://tailwindcss.com)
- Charts by [Recharts](https://recharts.org)

---

**Happy Budgeting! 💰**

If you find this project helpful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features
- 🤝 Contributing code
