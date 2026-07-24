# AetherLearn | AI-Powered Learning Platform

## Overview

**AetherLearn** is a modern, interactive web-based learning platform designed to deliver personalized AI-powered education in machine learning, deep learning, and prompt engineering. It combines video lessons, interactive quizzes, AI tutoring, progress tracking, and gamification to create an engaging learning experience.

The platform features a sophisticated dark/light theme system, real-time visualization of neural networks, and an immersive focus studio for deep work sessions.

---

## Features

### 🎓 Core Learning Modules

- **Structured Courses**: Multi-lesson modules covering AI fundamentals, neural networks, transformers, and advanced prompt engineering
- **Interactive Video Player**: Canvas-based video simulation with mathematical formula visualization and real-time network node animations
- **Dynamic Quizzes**: Instant feedback quizzes with XP rewards and personalized AI coaching
- **Lesson Notes**: Timestamp-linked personal notes synchronized with video playback
- **AI Transcript**: Clickable lesson transcripts for quick navigation

### 🤖 AI Tutor & Mentor

- **AI Study Copilot**: Chat-based assistant for homework help, concept explanations, and flashcard generation
- **Flashcard System**: Spaced repetition learning with flip animations and mastery tracking
- **Live Mentor Sessions**: Real-time conversational guidance with AetherIA featuring:
  - Audio waveform indicators
  - Shared whiteboard for notes
  - Live transcript recording
  - Agenda tracking

### 📊 Progress & Analytics

- **Interactive Dashboard**: Real-time stats on study hours, quiz accuracy, and rank level
- **Personalized Learning Path**: SVG-based node map showing curriculum progression with visual status indicators
- **Analytics Dashboard**: 
  - Weekly study activity line chart
  - Skill breakdown radar chart
  - GitHub-style contribution heatmap calendar
- **Achievement Trophy Room**: 15+ collectible badges with rarity tiers (Bronze → Platinum)

### 🧠 Knowledge Systems

- **Knowledge Constellation**: Interactive SVG graph showing concept interconnections across mathematics, ML, and engineering
- **Dynamic Skill Assessment**: Onboarding quiz to personalize learning difficulty and unlock appropriate content

### ⏱️ Focus Studio

- **Pomodoro Timer**: Customizable focus sessions (25 min), short (5 min), or long (15 min) breaks
- **Ambient Particle System**: Animated background particles for immersive focus environment
- **Multi-Ring Progress Tracking**: Circular progress indicators for:
  - Current session progress
  - Daily focus goals (4 sessions target)
  - Weekly study minutes (600 min target)
- **Task Labeling**: Custom focus task descriptions

### 🎮 Gamification

- **XP System**: Earn experience points from lessons, quizzes, and goals
- **Daily Goals**: Customizable daily targets with progress bars
- **Streak Tracking**: 7-day streak counter with visual ring indicators
- **Achievement Wall**: Tiered trophies with progress indicators and hidden achievements

---

## Technical Architecture

### Design System

The platform uses a comprehensive CSS variable system supporting both dark and light themes:

```css
--bg-primary: #090d16 (dark) | #f8fafc (light)
--accent-indigo: #6366f1
--accent-cyan: #06b6d4
--accent-success: #10b981
--accent-warning: #f59e0b
--accent-error: #ef4444
```

### Key Technologies

- **HTML5 Canvas**: Custom video player with real-time SVG network visualization
- **SVG Graphics**: Interactive charts, node maps, and knowledge graphs
- **CSS3 Animations**: Smooth transitions, keyframe animations, and 3D transforms
- **Vanilla JavaScript**: No framework dependencies — fully custom state management
- **LocalStorage**: Persistent user progress and state management

### Core Components

1. **Navigation System** (`sidebar`, `nav-links`): Multi-page routing with active state tracking
2. **Video Player** (`playerCanvas`, `drawVideoSimulation`): Canvas-based mock video with:
   - Mathematical formula cycling
   - Network node pulses
   - Signal propagation visualization
   - Scrolling code simulation
3. **Quiz Engine** (`state.quizState`): Question progression, answer tracking, and grading
4. **SVG Renderers**:
   - `renderPathMap()`: Learning node network visualization
   - `renderLineChart()`: Study activity line graph
   - `renderRadarChart()`: Skills breakdown radar
   - `renderKnowledgeGraph()`: Concept interconnection graph
5. **State Management** (`state` object): Centralized app state with auto-save to localStorage

---

## File Structure

```
AI_plateform.html
├── HTML Structure
│   ├── Sidebar Navigation
│   ├── Header Bar (Search, stats, theme toggle)
│   └── Content Container (7 main pages)
├── Embedded CSS (1800+ lines)
│   ├── Design system variables
│   ├── Component styles
│   └── Animation keyframes
└── Embedded JavaScript (2200+ lines)
    ├── State management
    ├── Navigation routing
    ├── Player controllers
    ├── Quiz engine
    └── Chart renderers
```

---

## Main Pages

### 1. **Dashboard** (`#page-dashboard`)
- Welcome banner with resume last lesson button
- 3-ring streak visualization
- Recent activity feed
- Daily focus goals
- Study statistics (hours, accuracy, level)
- Next milestone course previews

### 2. **Courses** (`#page-courses`)
- Filterable course catalog (by difficulty/category)
- Course cards with progress bars
- Difficulty badges

### 3. **Course Player** (`#view-course-player`)
- Full-screen video player with canvas rendering
- Tabs: About, Notes, Transcript, Quiz
- Interactive syllabus sidebar
- Note-taking with timestamp sync
- Built-in quiz challenges

### 4. **AI Tutor** (`#page-tutor`)
- Chat workspace for questions
- AI response generation with typing indicator
- Flashcard revision deck (right panel)
- Card flip animation
- Mastery tracking

### 5. **Learning Path** (`#page-path`)
- Onboarding assessment (3-step wizard)
- Interactive SVG node map
- Node popover details
- Path reset functionality

### 6. **AI Mentor** (`#page-mentor`)
- 3-column layout: agenda, live stage, transcript
- Animated AI consciousness orb
- Speaking waveform indicator
- Live transcript feed
- Session timer and recording indicator

### 7. **Achievement Wall** (`#page-achievements`)
- 15 collectable achievements with rarity tiers
- Progress bars for incomplete achievements
- Detail panel with criteria and rewards
- Category filtering

### 8. **Knowledge Graph** (`#page-graph`)
- 15 interconnected concept nodes
- Color-coded by domain (math, ML, engineering, applied)
- Search/filter functionality
- Detail cards on hover
- Link highlighting on node interaction

### 9. **Progress Analytics** (`#page-analytics`)
- 7-day study activity line chart
- 5-skill radar chart (Math, Programming, DeepLearning, MLOps, PromptEngineering)
- 52-week contribution heatmap calendar

### 10. **Focus Studio** (`#focus-studio-overlay`)
- Modal overlay with ambient particles
- 3-ring progress indicator
- Pomodoro timer display
- Focus mode selection (Deep Focus, Short Break, Long Break)
- Session stats (streak, sessions today, weekly minutes)

---

## Default Data

### Sample Courses

Three pre-built courses with lessons and quizzes:

1. **Introduction to Generative AI** (Beginner)
   - 4 lessons covering foundation models, transformers, LLMs vs. traditional ML, ethics
   - 3-question quiz (100 XP reward)

2. **Deep Neural Networks & Optimization** (Intermediate)
   - 4 lessons on backpropagation, loss functions, regularization, batch normalization
   - 3-question quiz (300 XP reward)

3. **Advanced Prompt Engineering** (Advanced)
   - 4 lessons on few-shot learning, ReAct framework, prompt injections, DSPy
   - 3-question quiz (400 XP reward)

### User Profile (Default)
```javascript
{
  name: "Learner One",
  level: 2,
  xp: 2450,
  streak: 5 days,
  skills: { Math: 65, Programming: 70, DeepLearning: 55, MLOps: 30, PromptEngineering: 45 }
}
```

### Daily Goals
- Complete 1 new lesson (0/1)
- Consult AI Tutor (0/1)
- Earn 100 Quiz XP (0/100)

---

## How to Use

### Getting Started

1. **Open the HTML file** in a modern web browser (Chrome, Firefox, Edge, Safari)
2. **Theme Toggle**: Click the theme button in sidebar to switch between dark/light modes
3. **Navigation**: Click sidebar items to explore different sections

### Taking a Course

1. Navigate to **Courses** page
2. Click a course card to enter the course player
3. Watch the interactive video lesson (click play button or center overlay)
4. Take notes with timestamp sync
5. Read the AI-generated transcript
6. Complete the built-in quiz

### Using the AI Tutor

1. Go to **AI Tutor** page
2. Click a suggestion chip or type your question
3. Wait for AI response with explanation
4. Generate flashcards from the response
5. Study cards using the flip interaction

### Tracking Progress

- **Dashboard**: Overview of daily goals and stats
- **Analytics**: Charts showing study patterns and skill development
- **Achievement Wall**: View collected and pending trophies
- **Learning Path**: See your curriculum progression visually

### Focus Sessions

1. Click the **focus icon** in header (or press Focus Studio button)
2. Optionally customize your task name
3. Select focus mode (25 min, 5 min, or 15 min)
4. Click play to start timer
5. Rings track progress across session/daily/weekly goals

---

## State Management

The app uses a single `state` object persisted to localStorage:

```javascript
state = {
  theme: 'dark',
  user: { name, level, xp, streak },
  courses: [...DEFAULT_COURSES],
  activeCourseId: null,
  activeLessonIndex: 0,
  notes: [],
  quizState: { active, questionIndex, userAnswers, completed },
  aiChatHistory: [],
  flashcards: [],
  activeCardIndex: 0,
  onboarding: { completed, goal, skillLevel, mathBackground },
  dailyGoals: [],
  studyStats: [],
  skills: {},
  focusSessionsToday: 0,
  focusWeeklyMins: 0,
  selectedAchievementId: null
}
```

**Key Functions:**
- `saveState()`: Persist to localStorage
- `loadState()`: Restore from localStorage
- `addXP(amount)`: Add XP and check for level up
- `updateGoalProgress(goalId, increment)`: Track daily goal completion

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Enter` (in chat) | Send message to AI tutor |
| `Enter` (in mentor chat) | Send message to mentor |
| `Click play button` | Start/pause video lesson |
| `Click timeline` | Seek video to position |
| `Click flashcard` | Flip card to see answer |

---

## Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ⚠️ Requires CSS Grid, CSS Custom Properties, SVG support, Canvas API

---

## Customization Guide

### Adding New Courses

Edit the `DEFAULT_COURSES` array in the JavaScript section:

```javascript
const DEFAULT_COURSES = [
  {
    id: "course-4",
    title: "Your Course Title",
    category: "Category Name",
    desc: "Description",
    difficulty: "beginner|intermediate|advanced",
    duration: "3.5 hrs",
    rating: "4.8",
    progress: 0,
    lessons: [
      { name: "Lesson 1", duration: "8 mins", completed: false, desc: "..." },
      // more lessons
    ],
    quiz: {
      xpReward: 200,
      completed: false,
      questions: [
        { question: "...", options: ["A", "B", "C", "D"], correctIndex: 1, explanation: "..." }
      ]
    }
  }
];
```

### Modifying Colors

Edit CSS variables in `:root` selector:

```css
:root {
  --accent-indigo: #6366f1;
  --accent-cyan: #06b6d4;
  /* etc */
}
```

### Adding Achievements

Edit the `ACHIEVEMENTS` array in the JavaScript section to add new trophy definitions.

### Customizing Focus Durations

Modify the `focusDurations` object:

```javascript
const focusDurations = {
  focus: 25 * 60,    // 25 minutes
  short: 5 * 60,     // 5 minutes
  long: 15 * 60      // 15 minutes
};
```

---

## Known Limitations

1. **Single File Architecture**: All code is in one HTML file (no bundling/module system)
2. **Mock Data**: Video player and AI responses are simulated (no real backend)
3. **LocalStorage Limits**: Browser storage cap (~5-10MB)
4. **Canvas Performance**: Many particles/nodes may impact performance on older devices
5. **No Persistence**: Data resets on browser data clear

---

## Future Enhancements

- [ ] Backend API integration for real courses
- [ ] WebRTC for live video mentor sessions
- [ ] Mobile-responsive design
- [ ] Real video streaming support
- [ ] Social features (peer learning groups)
- [ ] Certification generation
- [ ] Mobile app version
- [ ] Real-time collaboration on whiteboards
- [ ] Integration with external ML libraries (TensorFlow.js)
- [ ] Advanced analytics dashboard

---

## License

This project is provided as-is for educational purposes.

---

## Support & Contact

For issues, questions, or suggestions regarding AetherLearn, please refer to the inline documentation within the HTML file.

---

**Last Updated**: July 2026  
**Version**: 1.0.0  
**Platform**: Web (HTML5, CSS3, Vanilla JavaScript)
