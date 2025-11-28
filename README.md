# AI Short Video Creator - Frontend

## 📋 Project Description

A modern web application for AI-powered short video creation built with Next.js and React. This frontend provides an intuitive step-by-step workflow for users to create professional short-form videos automatically using AI, from topic selection through script generation, voice narration, background selection, to final video export and social media sharing.

## 🚀 Key Features

### User Authentication & Profile

- User registration and login
- OAuth integration (Google, Facebook)
- Profile management and settings
- Secure session handling with JWT

### Video Creation Workflow

- **Topic Selection**: Browse trending topics or create custom topics
- **AI Script Generation**: Generate and customize video scripts with AI
- **Voice Selection**: Choose from 30+ premium voices with preview
- **Background Selection**: Pick from image library or upload custom backgrounds
- **Multi-Scene Support**: Create videos with multiple background images
- **Subtitle Customization**: Multiple subtitle styles and positioning options
- **Real-time Preview**: Preview video before final generation

### Media Management

- Upload and organize media files (images, audio, video)
- Media library with categorization and search
- Cloud-based storage integration
- Media type validation and preview

### Social Media Integration

- Direct video publishing to Facebook, TikTok, and YouTube
- Facebook page management
- Video analytics and performance tracking
- Multi-platform sharing capabilities

### Dashboard & Analytics

- View all created videos
- Video status tracking (processing, completed, failed)
- Edit, delete, and share options
- Performance metrics and engagement stats

## 🛠️ Tech Stack

- **Framework**: Next.js 14+ (React 18+)
- **Language**: TypeScript
- **Styling**: TailwindCSS
- **State Management**: React Context API, Zustand
- **API Integration**: Axios, SWR for data fetching
- **Form Handling**: React Hook Form
- **Authentication**: NextAuth.js
- **UI Components**: Custom components with Tailwind
- **Icons**: React Icons
- **Development**: ESLint, Prettier

## 📁 Project Structure

```
Software-Design-FE/
├── public/
│   ├── assets/
│   │   ├── images/          # Static images
│   │   └── videos/          # Static videos
│   ├── fonts/               # Custom fonts
│   ├── stickers/            # Sticker assets
│   └── preview-style/       # Preview templates
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── common/          # Shared components
│   │   ├── layout/          # Layout components
│   │   ├── video/           # Video-related components
│   │   └── dashboard/       # Dashboard components
│   ├── context/             # React Context providers
│   │   ├── AuthContext.tsx  # Authentication state
│   │   ├── VideoContext.tsx # Video creation state
│   │   └── MediaContext.tsx # Media management state
│   ├── hooks/               # Custom React hooks
│   │   ├── useAuth.ts
│   │   ├── useVideo.ts
│   │   └── useMedia.ts
│   ├── pages/               # Next.js pages (App Router)
│   │   ├── index.tsx        # Home page
│   │   ├── auth/            # Authentication pages
│   │   ├── create/          # Video creation flow
│   │   ├── dashboard/       # User dashboard
│   │   └── api/             # API routes
│   ├── services/            # API service layer
│   │   ├── auth.service.ts
│   │   ├── video.service.ts
│   │   ├── media.service.ts
│   │   └── social.service.ts
│   ├── styles/              # Global styles
│   │   └── globals.css
│   ├── types/               # TypeScript type definitions
│   │   ├── user.types.ts
│   │   ├── video.types.ts
│   │   └── media.types.ts
│   └── utils/               # Utility functions
│       ├── api.ts           # API client setup
│       ├── validators.ts    # Form validators
│       └── formatters.ts    # Data formatters
├── .env.local               # Environment variables
├── next.config.js           # Next.js configuration
├── tailwind.config.js       # Tailwind CSS configuration
├── tsconfig.json            # TypeScript configuration
└── package.json             # Dependencies
```

## 🔧 Installation

1. **Clone the repository**

```bash
git clone https://github.com/DucToan137/ai-short-video-creator-fe.git
cd ai-short-video-creator-fe
```

2. **Install dependencies**

```bash
npm install
# or
yarn install
```

3. **Configure environment variables**
   Create a `.env.local` file in the root directory:

```env
# API Configuration
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_API_BASE_URL=http://127.0.0.1:8000
NEXT_PUBLIC_ENV=development
```

4. **Start the development server**

```bash
npm run dev
# or
yarn dev
```

5. Open your browser and navigate to [http://localhost:3000](http://localhost:3000)

### Build for Production

```bash
npm run build
npm run start
# or
yarn build
yarn start
```

## 📚 Main Routes

### Public Routes

- `/` - Landing page with features showcase
- `/auth/login` - User login page
- `/auth/register` - User registration page
- `/auth/forgot-password` - Password recovery

### Protected Routes

- `/dashboard` - User dashboard with video library
- `/create/topic` - Topic selection step
- `/create/script` - Script generation and editing
- `/create/voice` - Voice selection and preview
- `/create/background` - Background image selection
- `/create/preview` - Video preview and customization
- `/create/export` - Export and publishing options

### Media Management Routes

- `/media` - Media library overview
- `/media/upload` - Upload media files
- `/media/images` - Image gallery
- `/media/audio` - Audio files
- `/media/videos` - Video files

### Social Media Routes

- `/social/connect` - Connect social media accounts
- `/social/facebook` - Facebook page management
- `/social/analytics` - Social media analytics

### Settings Routes

- `/settings/profile` - User profile settings
- `/settings/account` - Account settings
- `/settings/preferences` - App preferences

## 🎨 Key Components

### Video Creation Components

- `TopicSelector` - Trending topics and custom topic input
- `ScriptEditor` - AI-generated script editing interface
- `VoiceSelector` - Voice preview and selection
- `BackgroundGallery` - Background image selection
- `VideoPreview` - Real-time video preview
- `SubtitleCustomizer` - Subtitle style customization
- `ExportPanel` - Video export and sharing options

### Dashboard Components

- `VideoCard` - Individual video display card
- `VideoGrid` - Grid layout for video library
- `StatusBadge` - Video processing status indicator
- `AnalyticsChart` - Video performance charts

### Common Components

- `Navbar` - Navigation bar with auth status
- `Sidebar` - Dashboard sidebar navigation
- `Modal` - Reusable modal component
- `Button` - Customizable button component
- `Input` - Form input components
- `Loader` - Loading indicators

## 🔐 Authentication Flow

1. User registers or logs in (email/password or OAuth)
2. JWT token received from backend
3. Token stored in secure HTTP-only cookie
4. Protected routes check authentication status
5. Automatic token refresh on expiration

## 🎥 Video Creation Flow

1. **Topic Selection** → Choose or create topic
2. **Script Generation** → AI generates script from topic
3. **Script Editing** → Customize generated script
4. **Voice Selection** → Choose voice and preview
5. **Background Selection** → Pick background images
6. **Preview & Customize** → Preview video and adjust settings
7. **Generate Video** → Backend processes video
8. **Export & Share** → Download or publish to social media

## 🗄️ State Management

- **AuthContext**: User authentication state
- **VideoContext**: Video creation workflow state
- **MediaContext**: Media library and uploads
- **SocialContext**: Social media connections
- **NotificationContext**: App-wide notifications

## 🔒 Security Features

- Secure authentication with JWT
- HTTP-only cookies for token storage
- CSRF protection
- Input validation and sanitization
- Protected API routes
- Secure OAuth flow

## 🧪 Testing & Development

```bash
# Run development server
npm run dev

# Build for production
npm run build

# Run linter
npm run lint

# Fix linting issues
npm run lint:fix

# Type checking
npm run type-check
```

## 📄 License

This project is licensed under the MIT License.
