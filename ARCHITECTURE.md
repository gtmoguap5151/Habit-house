# Habit House - System Architecture

## 1. App Structure (Screens)

### 1.1 Onboarding Flow
- Welcome Screen
- Goal Selection Screen
- Schedule Input Screen
- Habit Selection Screen
- AI Setup Complete Screen

---

### 1.2 Main App (Core UI)

#### Home Dashboard
- Today’s AI Plan
- 3–7 suggested actions
- Progress streak
- Quick add habit button

#### Habits Screen
- List of habits
- Progress tracking
- Streak counters
- Completion toggle

#### AI Coach Screen
- Chat-style AI interface
- Daily feedback
- Suggestions
- Motivation messages

#### Insights Screen
- Weekly progress
- Habit success rate
- Behavior patterns

#### Profile/Settings
- Goals
- Subscription
- Notifications
- Integrations

---

## 2. Database Structure (Firebase)

### Users
- user_id
- name
- email
- goals
- created_at

### Habits
- habit_id
- user_id
- title
- frequency
- streak
- status

### Daily Plans
- plan_id
- user_id
- date
- tasks[]
- completion_status

### AI Logs
- log_id
- user_id
- input
- response
- timestamp

---

## 3. AI System Design

### AI Role: Personal Life Operating System

The AI performs 4 core functions:

1. Planner
   - Builds daily schedule

2. Coach
   - Gives feedback
   - Adjusts habits

3. Analyzer
   - Finds behavior patterns

4. Motivator
   - Encourages consistency
   - Prevents burnout

---

## 4. AI Rules

- Never overwhelm the user
- Prefer small actions over big goals
- Adjust difficulty automatically
- Reinforce consistency
- Learn from missed habits without punishment tone

---

## 5. Data Flow

User Action → Firebase → AI Analysis → Updated Plan → UI Refresh

---

## 6. Future Integrations (Hardware Ready)

- Smartwatches
- Fitness trackers
- Calendar APIs
- Voice assistants
- Sleep tracking devices
- GPS-based habits
- 
