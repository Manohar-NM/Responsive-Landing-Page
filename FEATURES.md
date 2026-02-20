# Features & Functionality Guide

## 🎯 Landing Page Features

### 1. Header & Navigation

#### Desktop View
- Fixed sticky navigation bar
- Logo on the left (clickable, returns to home)
- Navigation menu with links: Home, Features, Contact
- Smooth hover effects on links

#### Mobile View
- Responsive hamburger menu icon
- Hamburger expands to show full menu
- Menu closes when a link is clicked
- Touch-friendly button sizes

**Code Location:** `index.html` (lines 1-20), `style.css` (lines 49-90), `script.js` (lines 1-25)

---

### 2. Hero Section

#### Visual Elements
- Gradient background (blue to dark blue)
- Large headline: "Welcome to SoftGrow Tech"
- Subtitle with value proposition
- White "Get Started" button
- Fade-in animation on page load

#### Functionality
- Hero title animates in when page loads
- Button click scrolls smoothly to features section
- Fully responsive text sizes for all devices
- Maintains aspect ratio on any screen

**Code Location:** `index.html` (lines 24-34), `style.css` (lines 112-158), `script.js` (lines 58-65)

---

### 3. Features Section

#### Layout
- Responsive grid layout (auto-adjusts columns)
- 6 feature cards displayed
- Equal spacing and padding
- Hover animations

#### Feature Cards Include
1. **Fast Performance** 🚀
   - Description: Lightning-fast loading times

2. **Beautiful Design** 🎨
   - Description: Modern responsive designs

3. **Secure & Reliable** 🔒
   - Description: Enterprise-grade security

4. **Mobile First** 📱
   - Description: Seamlessly adaptive design

5. **Easy Integration** ⚡
   - Description: Simple APIs and documentation

6. **24/7 Support** 💬
   - Description: Round-the-clock support

#### Hover Effects
- Cards lift up by 5px
- Shadow increases
- Smooth transition over 0.3 seconds

**Code Location:** `index.html` (lines 49-71), `style.css` (lines 160-195), `script.js` (lines 67-79)

---

### 4. Footer with Contact Information

#### Sections
1. **About Us**
   - Company description
   - Mission statement

2. **Contact Information**
   - Email: info.softgrowtech@gmail.com
   - WhatsApp: +91 7839686310
   - Both are clickable links

3. **Quick Links**
   - Links to Home, Features, Contact
   - Consistent navigation

#### Features
- Dark background (#1f2937)
- Responsive 3-column grid
- Collapses to single column on mobile
- Footer bottom with copyright
- Hover effects on links

**Code Location:** `index.html` (lines 73-102), `style.css` (lines 197-240)

---

### 5. Responsive Design

#### Breakpoints
- **Desktop (1200px+):** Full layout with all features visible
- **Tablet (769px-1199px):** Adjusted spacing and font sizes
- **Mobile (481px-768px):** Stacked layout, hamburger menu
- **Small Mobile (<480px):** Minimal layout, extra-small fonts

#### Mobile Optimizations
- Hamburger menu replaces desktop nav
- Increased button sizes for touch
- Larger text for readability
- Full-width elements on small screens
- Vertical stacking of sections

**Code Location:** `style.css` (lines 242-300)

---

### 6. Interactive Features

#### Smooth Scrolling
- Click any navigation link
- Page smoothly scrolls to the target section
- Works on all browsers supporting scroll-behavior

#### Button Interactions
- CTA button has hover animation (lifts up)
- Shadow increases on hover
- Click feedback with transform

#### Animation
- Hero content fades in on load
- Feature cards fade in as you scroll
- All transitions are smooth (0.3s ease)

**Code Location:** `script.js` (lines 1-79)

---

## 📝 To-Do List App Features

### 1. Add Tasks

#### How It Works
- User types task text in input field
- Click "Add Task" button or press Enter key
- Task is added to the list
- Input field clears automatically
- Task persists in local storage

#### Validation
- Empty task cannot be added
- Shows alert if user tries to add empty task
- Auto-focus on input after adding task

**Code Location:** `todo-script.js` (lines 30-50)

---

### 2. Remove Tasks

#### How It Works
- Click "Delete" button next to any task
- Task is immediately removed
- Local storage is updated
- UI refreshes to show current state

#### Safety
- No confirmation for single delete
- But there's confirmation for "Clear Completed"

**Code Location:** `todo-script.js` (lines 52-56)

---

### 3. Mark as Completed

#### How It Works
- Click checkbox next to any task
- Task text gets strikethrough
- Task color becomes gray
- Completed count updates
- Status persists in local storage

#### Visual Feedback
- Checkbox becomes checked
- Task moves to "Completed" filter view
- Statistics update in real-time

**Code Location:** `todo-script.js` (lines 58-65)

---

### 4. Filter Tasks

#### Available Filters
- **All:** Shows all tasks (default view)
- **Active:** Shows only incomplete tasks
- **Completed:** Shows only finished tasks

#### How It Works
- Click filter button at top
- Active filter button is highlighted (blue)
- List updates to show filtered tasks
- Empty state message shown if no tasks in filter

#### Visual Changes
- Active filter button has blue background and white text
- Inactive buttons show blue border
- Smooth transitions when switching filters

**Code Location:** `todo-script.js` (lines 67-79), `todo-style.css` (lines 105-125)

---

### 5. Local Storage

#### What Gets Stored
- Task ID (timestamp-based)
- Task text
- Completion status
- Creation timestamp

#### How It Works
- Every change saves to localStorage automatically
- Data persists even after closing browser
- Clears only when user clears cache or "Clear Completed"
- Up to 5MB storage available

#### Storage Key
- `localStorage['todos']` - stores JSON array of tasks

**Code Location:** `todo-script.js` (lines 99-105)

---

### 6. Task Statistics

#### Real-time Statistics
- **Total:** Shows total number of tasks
- **Completed:** Shows number of completed tasks

#### How It Works
- Counts update automatically when tasks change
- Uses `querySelectorAll` to count completed tasks
- Updates instantly on every action

#### Visual Display
- Shows in bottom stats bar
- Bold numbers for emphasis
- Updates without page refresh

**Code Location:** `todo-script.js` (lines 89-96)

---

### 7. Clear Completed Tasks

#### Functionality
- Removes all completed tasks at once
- Shows confirmation dialog
- Updates storage and UI
- Button is disabled if no completed tasks

#### Safety Features
- Confirmation prompt before clearing
- Button is greyed out when inactive
- Status message shows how many tasks will be cleared

**Code Location:** `todo-script.js` (lines 81-88)

---

### 8. Empty State Message

#### Displays When
- No tasks exist in the entire list
- No tasks match current filter

#### Message
- Shows: "✨ No tasks yet. Add one to get started!"
- Encourages user to add first task
- Disappears when tasks are added

**Code Location:** `todo-script.js` (lines 91-99)

---

### 9. Security Features

#### XSS Protection
- Task text is escaped using textContent
- Prevents HTML injection
- Sanitizes all user input

#### How It Works
```javascript
const div = document.createElement('div');
div.textContent = userInput;
return div.innerHTML; // Safe HTML
```

**Code Location:** `todo-script.js` (lines 106-110)

---

### 10. User Experience Features

#### Keyboard Support
- Press Enter to add task
- Tab navigation between buttons
- Accessible form controls

#### Responsive Layout
- Mobile-first design
- Touch-friendly buttons
- Large input field
- Flexible card layout

#### Visual Feedback
- Animations on task add/remove
- Color changes on completion
- Button hover effects
- Loading states

**Code Location:** `todo-style.css` (lines 1-250), `todo-script.js` (entire file)

---

## 🎨 Design Features

### Landing Page
- **Color Palette:** Blue (#2563eb), Dark Blue (#1e40af)
- **Typography:** Segoe UI, sans-serif
- **Spacing:** Consistent 1rem gaps
- **Shadows:** Subtle shadows for depth
- **Animations:** Smooth 0.3s transitions

### To-Do App
- **Color Palette:** Blue, Green, Red (for actions)
- **Gradient Background:** Purple gradient
- **Card Design:** White cards on gradient background
- **Smooth Animations:** Slide-in effects
- **Modern UI:** Rounded corners, clean spacing

---

## 📊 Technical Implementation

### Technologies Used
- **HTML5:** Semantic elements for accessibility
- **CSS3:** Flexbox and Grid for layouts
- **JavaScript ES6:** Modern syntax with classes
- **Local Storage API:** Client-side data persistence
- **Intersection Observer:** Efficient scroll animations

### Code Quality
- Clean, readable code with comments
- DRY (Don't Repeat Yourself) principles
- Object-oriented approach in to-do app
- Event delegation for efficiency

---

## ✅ Feature Checklist

### Landing Page
- [x] Sticky header navigation
- [x] Hamburger menu for mobile
- [x] Hero section with CTA
- [x] 6 feature cards
- [x] Footer with contact info
- [x] Responsive design
- [x] Smooth animations
- [x] Cross-browser compatible

### To-Do App
- [x] Add tasks
- [x] Remove tasks
- [x] Mark as completed
- [x] Filter tasks (All/Active/Completed)
- [x] Local storage persistence
- [x] Task statistics
- [x] Clear completed tasks
- [x] XSS protection
- [x] Responsive design
- [x] Keyboard support

---

**Version:** 1.0.0  
**Last Updated:** February 20, 2026
