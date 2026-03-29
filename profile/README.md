# 🎓 GB Career Pilot - AI-Powered University Counseling Platform

<div align="center">

![GB Career Pilot](https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-Dual%20License-blue?style=for-the-badge)
![Contributors](https://img.shields.io/badge/Contributors-Welcome-orange?style=for-the-badge)
![Students](https://img.shields.io/badge/Made%20By-Students-purple?style=for-the-badge)

**Empowering Pakistani Students with AI-Powered Career Guidance**

[Live Demo](https://raqeebs.app) • [Documentation](./PROJECT_STATUS_COMPLETE.md) • [Roadmap](./ROADMAP.md) • [Contributing](./CONTRIBUTING.md) • [Discord](#)

</div>

---

## 🌟 What is GB Career Pilot?

**GB Career Pilot** is an open-source, AI-powered university counseling platform designed to help Pakistani students make informed decisions about their academic future. Using cutting-edge AI technology, we provide:

✨ **Intelligent Career Counseling** - Chat with an AI counselor 24/7  
🎓 **Comprehensive University Database** - Search and compare Pakistani universities  
📚 **Program Discovery** - Find programs that match your interests and goals  
💰 **Cost Analysis** - Understand tuition fees and financial requirements  
📊 **Personalized Dashboard** - Track your university search journey  
🔒 **Secure & Private** - Your data is safe with enterprise-grade security  

---

## 🚀 Quick Start

### Try It Live

**🌐 Visit:** [https://raqeebs.app](https://raqeebs.app)

No installation needed! Create an account and start exploring.

### Run Locally

#### Prerequisites
- **Node.js** 18+ and npm
- **Python** 3.10+
- **PostgreSQL** (or use Supabase)
- **Redis** (or use Upstash)

#### Backend Setup

```bash
# Clone the repository
git clone https://github.com/FeelAndSupport/gb-career-pilot.git
cd gb-career-pilot/gb-career-pilot-backend

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Setup environment variables
cp .env.example .env
# Edit .env with your credentials (see Environment Setup below)

# Run database migrations (if needed)
alembic upgrade head

# Start the server
uvicorn src.main:app --reload
```

Backend will run at: `http://localhost:8000`

#### Frontend Setup

```bash
# Navigate to frontend directory
cd gb-career-pilot-frontend

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env
# Edit .env with your API URL

# Start development server
npm run dev
```

Frontend will run at: `http://localhost:5173`

#### Environment Setup

See [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md) for detailed environment variable setup.

**Required variables:**
- `SUPABASE_URL` and `SUPABASE_SERVICE_KEY` - Database
- `GROQ_API_KEY` - AI service
- `UPSTASH_REDIS_URL` and `UPSTASH_REDIS_TOKEN` - Caching
- `JWT_SECRET_KEY` and `JWT_REFRESH_SECRET_KEY` - Authentication
- Email service API keys (Resend/Brevo/Mailgun)

---

## 🎯 Features

### For Students

🤖 **AI Career Counselor**
- Ask questions about universities, programs, careers
- Get personalized recommendations
- Conversation history saved
- Available 24/7

🔍 **University Search**
- 200+ Pakistani universities (growing!)
- Filter by location, ranking, programs
- Detailed information and requirements
- Save favorite universities

📚 **Program Discovery**
- Search programs by field, degree level
- Compare tuition fees and duration
- View admission requirements
- Explore career prospects

👤 **Personal Dashboard**
- Track your university search
- Save universities and programs
- View statistics and insights
- Manage your profile

### For Developers

⚡ **Modern Tech Stack**
- Frontend: React 19, Vite 8, Tailwind CSS 4
- Backend: FastAPI, Python 3.14
- Database: PostgreSQL (Supabase)
- Cache: Redis (Upstash)
- AI: Groq Llama 3.3 70B

🔧 **Developer-Friendly**
- Well-documented codebase
- Comprehensive API documentation
- Easy local setup
- Active community support

🎨 **Beautiful Design**
- Custom "Sunrise Scholar" design system
- Responsive and accessible
- Smooth animations
- Modern UI components

---

## 📊 Tech Stack

### Frontend
```
React 19.2.4          │ Modern UI library
Vite 8.0.1            │ Lightning-fast build tool
Tailwind CSS 4.2.2    │ Utility-first CSS
TanStack Query 5.x    │ Data fetching & caching
React Router 7.x      │ Client-side routing
Zod 4.x               │ Schema validation
React Hook Form 7.x   │ Form management
```

### Backend
```
FastAPI 0.110.0       │ High-performance web framework
Python 3.14.2         │ Latest Python
Pydantic 2.7.0        │ Data validation
Supabase 2.11.0       │ PostgreSQL database
Upstash Redis 0.15.0  │ Serverless caching
Groq 0.4.2            │ Ultra-fast AI inference
LangChain 0.1.11      │ LLM framework
PyJWT 2.8.0           │ Authentication
```

### Infrastructure
```
Vercel                │ Frontend hosting
Render                │ Backend hosting
Supabase              │ Managed PostgreSQL
Upstash               │ Serverless Redis
Sentry                │ Error monitoring
```

**📖 Full Details:** [COMPLETE_TECH_STACK.md](./COMPLETE_TECH_STACK.md)

---

## 📁 Project Structure

```
gb-career-pilot/
├── 📂 gb-career-pilot-backend/      # FastAPI Backend
│   ├── src/
│   │   ├── api/v1/endpoints/        # API routes
│   │   │   ├── ai_endpoints.py      # AI chat
│   │   │   ├── auth.py              # Authentication
│   │   │   ├── universities.py      # University data
│   │   │   └── users.py             # User management
│   │   ├── cache/                   # Redis client
│   │   ├── database/                # Database models
│   │   ├── services/                # Business logic
│   │   └── main.py                  # App entry point
│   ├── tests/                       # Backend tests
│   └── requirements.txt             # Python dependencies
│
├── 📂 gb-career-pilot-frontend/     # React Frontend
│   ├── src/
│   │   ├── pages/                   # React pages
│   │   │   ├── Home.jsx             # Landing page
│   │   │   ├── auth/                # Login, Register
│   │   │   ├── dashboard/           # User dashboard
│   │   │   ├── chat/                # AI chat
│   │   │   └── universities/        # University search
│   │   ├── components/              # React components
│   │   ├── hooks/                   # Custom hooks
│   │   ├── services/                # API services
│   │   └── App.jsx                  # Main app
│   ├── tests/                       # Frontend tests
│   └── package.json                 # Node dependencies
│
├── 📄 LICENSE.md                    # Dual-license
├── 📄 CONTRIBUTING.md               # Contribution guide
├── 📄 CODE_OF_CONDUCT.md            # Community guidelines
├── 📄 ROADMAP.md                    # Project roadmap
└── 📄 README.md                     # This file
```

---

## 🤝 Contributing

We're a **student-led open source project** under **Feel and Support** organization, and we ❤️ contributions!

### How to Contribute

1. **Join our Discord:** [[Discord Invite Link]](https://discord.gg/Y2Mka3Ah) 
2. **Read:** [CONTRIBUTING.md](./CONTRIBUTING.md)
3. **Pick an issue:** Look for `good first issue` label
4. **Submit PR:** Follow our contribution guidelines

### Contribution Areas

- 💻 **Frontend** - React, UI/UX, Design
- ⚙️ **Backend** - Python, FastAPI, APIs
- 🤖 **AI/ML** - LangChain, Prompt Engineering
- 📊 **Data** - University data entry, verification
- 📝 **Docs** - Documentation, tutorials
- 🎨 **Design** - UI mockups, graphics
- 🧪 **Testing** - Write tests, QA
- 🌍 **Translation** - Urdu, Arabic, others

### Recognition

Contributors get:
- ✅ Listed in [CONTRIBUTORS.md](./CONTRIBUTORS.md)
- ✅ Discord contributor role
- ✅ Mentioned in release notes
- ✅ Featured on our website
- ✅ Recommendation letters (upon request)

---

## 📜 License

**Dual-License Model:**

- 🆓 **Free for Non-Profit Use** - Students, educational institutions, NGOs
- 💼 **Commercial License Required** - For-profit businesses

See [LICENSE.md](./LICENSE.md) for full details.

For commercial licensing inquiries: [contact@feelandsupport.org]

---


## 🏆 Project Stats

![Lines of Code](https://img.shields.io/badge/Lines%20of%20Code-6.6k+-blue)
![Backend](https://img.shields.io/badge/Backend-2.4k%20lines-green)
![Frontend](https://img.shields.io/badge/Frontend-4.2k%20lines-orange)
![Documentation](https://img.shields.io/badge/Docs-72%20files-purple)

**Code Quality:**
- ✅ Production Ready
- ✅ Well Documented
- ✅ Actively Maintained
- ✅ Test Coverage (Growing)

---

## 🌍 Community

### Join Us

- 💬 **Discord:** https://discord.gg/Y2Mka3Ah
- 🐦 **Twitter:** [@GBCareerPilot]
- 📧 **Email:** contact@feelandsupport.org
- 🌐 **Website:** [feelandsupport.org]

### Stay Updated

- ⭐ **Star this repo** to follow updates
- 👁️ **Watch** for notifications
- 🔔 **Subscribe** to releases
- 📰 **Follow** on social media

---

## 🙏 Acknowledgments

### Core Team
- **Raqeeb** - Founder & Lead Developer

### Special Thanks
- **Groq** - For ultra-fast AI inference
- **Supabase** - For database infrastructure
- **Vercel** - For frontend hosting
- **All contributors** - For making this possible!

### Built With
Special thanks to the creators of:
- React, Vite, Tailwind CSS
- FastAPI, Python
- PostgreSQL, Redis
- LangChain, Groq

---

## 📞 Contact & Support

### For Users
- 🐛 **Bug Reports:** [GitHub Issues](../../issues)
- 💡 **Feature Requests:** [GitHub Discussions](../../discussions)
- ❓ **Questions:** [Discord #help]

### For Contributors
- 💬 **Chat:** [Discord #general]
- 📧 **Email:** contributors@feelandsupport.org
- 🤝 **Mentorship:** [Discord #mentorship]

### For Organizations
- 🤝 **Partnerships:** partnerships@feelandsupport.org
- 💼 **Commercial License:** licensing@feelandsupport.org
- 📊 **Sponsorship:** sponsorship@feelandsupport.org

---

## 🔒 Security

Found a security vulnerability? Please **do not** open a public issue.

Email: security@feelandsupport.org

See [SECURITY.md](./SECURITY.md) for our security policy.

---

## 📈 Project Activity

![GitHub last commit](https://img.shields.io/github/last-commit/GB-AI-Tutor/gb-career-pilot-backend)
![GitHub issues](https://img.shields.io/github/issues/FeelAndSupport/gb-career-pilot)
![GitHub pull requests](https://img.shields.io/github/issues-pr/FeelAndSupport/gb-career-pilot)

---

## 💖 Support the Project

### Contribute
The best way to support us is to contribute! See [CONTRIBUTING.md](./CONTRIBUTING.md)

### Spread the Word
- ⭐ Star this repository
- 🐦 Share on social media
- 📝 Write about us
- 🎥 Create tutorials

### Sponsor
Interested in sponsoring? Contact: raqeebraees23@gmail.com

---

## 📄 Citation

If you use GB Career Pilot in your research or project, please cite:

```bibtex
@software{gb_career_pilot_2026,
  title = {GB Career Pilot: AI-Powered University Counseling Platform},
  author = {Feel and Support Organization},
  year = {2026},
  url = {https://github.com/FeelAndSupport/gb-career-pilot}
}
```

---

## 🎓 About Feel and Support

**Feel and Support** is a student-led organization dedicated to empowering students through technology. We build open-source tools that make education more accessible and help students succeed.

**Mission:** Democratize access to quality educational guidance through technology.

**Vision:** Every student deserves the best tools to plan their future.

---

<div align="center">

### ⭐ Star us on GitHub — it motivates us a lot!

**Made with ❤️ by students, for students**

[Website](#) • [Discord](https://discord.gg/Y2Mka3Ah) • [Twitter](#) • [Email](2022n00020@gmail.com)

---

**GB Career Pilot** - Empowering Pakistani Students with AI 🚀

*Licensed under Dual-License | Copyright © 2026 Feel and Support*

</div>
