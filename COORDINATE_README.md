# 🤖 Coordinate AI LibreChat Integration

This is a customized LibreChat deployment pre-configured to work with your Coordinate AI Product Specification Agent.

## ✨ What This Gives You

- **ChatGPT-like interface** for product specification creation
- **Direct Notion integration** - creates epics, stories, and requirements in your workspace
- **Natural language commands** like "Create an epic for user authentication"
- **Team collaboration** with conversation history and shared sessions

## 🚀 Quick Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/librechat-coordinate)

### Manual Deployment

1. **Clone this repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/librechat-coordinate
   cd librechat-coordinate
   ```

2. **Deploy to Vercel**
   ```bash
   npm install -g vercel
   vercel
   ```

3. **Set Environment Variables in Vercel**
   - `ENDPOINTS=custom`
   - `COORDINATE_API_KEY=your-secure-key`
   - `APP_TITLE=Coordinate AI Product Spec Agent`

## 🐳 Docker Deployment

```bash
# 1. Clone and setup
git clone https://github.com/YOUR_USERNAME/librechat-coordinate
cd librechat-coordinate

# 2. Copy environment file
cp .env.example .env
# Edit .env with your settings

# 3. Run with Docker
docker-compose up -d
```

Access at: `http://localhost:3080`

## 🎯 How to Use

1. **Open LibreChat** (locally or on Vercel)
2. **Select "Coordinate AI Agent"** from the model dropdown
3. **Start typing natural language commands:**
   - "Create an epic for mobile app notifications"
   - "Generate user stories for checkout flow"
   - "What functional requirements do we need for search?"
   - "Add more stories to the authentication epic"

4. **Check your Notion workspace** - all items are created automatically!

## ⚙️ Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `ENDPOINTS` | Enable custom endpoints | `custom` |
| `COORDINATE_API_KEY` | API key for Coordinate AI | `your-secure-key` |
| `APP_TITLE` | Application title | `Coordinate AI Product Spec Agent` |
| `ALLOW_REGISTRATION` | Allow user registration | `true` |

### Custom Model Configuration

The `librechat.yaml` file is pre-configured with:
- **Base URL:** `https://coordinate-product-orchestration.vercel.app/api/librechat`
- **Models:** `ai-notion-agent`, `ai-product-assistant`
- **Custom system prompts** for product specification tasks

## 🔗 Integration Details

This LibreChat connects to your existing:
- ✅ **AI Notion Agent** (Supabase Edge Functions)
- ✅ **Notion Databases** (Epics, Stories, Requirements, Questions)
- ✅ **GitHub Sync** (Automatic relationship detection)
- ✅ **Production API** at coordinate-product-orchestration.vercel.app

## 📚 Usage Examples

### Epic Creation
```
User: "I need an epic for real-time collaboration features"
AI: ✅ Created epic + 3 stories + 2 questions in your Notion workspace
```

### Story Generation
```
User: "Generate user stories for file sharing functionality"
AI: ✅ Created 4 user stories with acceptance criteria in Notion
```

### Requirements Engineering
```
User: "What functional requirements do we need for search functionality?"
AI: ✅ Created detailed functional requirements with behaviors and constraints
```

## 🛠️ Development

```bash
# Local development
npm install
npm run dev

# Build for production
npm run build
npm start
```

## 📞 Support

- **API Issues:** Check https://coordinate-product-orchestration.vercel.app/api/librechat/models
- **Configuration:** Review `librechat.yaml` settings
- **Notion Integration:** Verify database IDs and permissions

---

**Ready to transform your product specification workflow!** 🚀