📒 NotesApp (Jetpack Compose + Firebase)
NotesApp is a modern note-taking Android app built using Jetpack Compose, Firebase Authentication, and Cloud Firestore. 

It supports:
Email/password login
Google Sign-In (One Tap)
Viewing and editing notes
Profile and note-taking statistics
✅ Features
🔐 Email & Password Authentication
🔑 Google One Tap Sign-In
🏠 Home screen with welcome message & recent notes
📝 Create, tag, and save notes
📊 Profile view with note statistics
🧭 Bottom navigation for quick access
💾 Firebase Firestore backend


🔐 Login Options
Email/Password Login
Register with email & password
Login using the same credentials
Google Sign-In
Tap “Sign in with Google”
Uses One Tap authentication
Requires valid WEB_CLIENT_ID
🛠 Tech Stack
Kotlin
Jetpack Compose
Firebase Authentication
Cloud Firestore
MVVM Architecture
Material 3 UI
Gradle Version Catalogs


📁 Project Structure (Complete with Descriptions)
NotesApp/
├── app/
│   ├── auth/
│   │   └── GoogleAuthUiClient.kt       # Handles Google One Tap authentication logic and integrates with FirebaseAuth
│
│   ├── components/
│   │   ├── BottomBar.kt                # Bottom navigation bar used across screens
│   │   └── FormattingButton.kt         # Rich text formatting button for styling note content
│
│   ├── data/
│   │   └── NotesRepository.kt          # Provides abstraction for interacting with Firestore (CRUD operations for notes)
│
│   ├── model/
│   │   └── Note.kt                     # Data class representing a note (title, content, tags, timestamp)
│   │   └── (TODO) User.kt              # (Suggestion) Add model for user data like display name, email, profile image
│
│   ├── navigation/
│   │   ├── AppNavigation.kt            # Contains top-level navigation setup and route configuration
│   │   └── NavGraph.kt                 # Defines composable destinations and screen transitions using Jetpack Navigation
│
│   ├── screens/
│   │   ├── auth/
│   │   │   ├── LoginScreen.kt          # UI for signing in using email/password or Google Sign-In
│   │   │   ├── ProfileScreen.kt        # Displays logged-in user's info, logout button, and placeholder for stats
│   │   │   └── RegisterScreen.kt       # UI for creating a new user account with email and password
│   │   ├── home/
│   │   │   ├── EditProfileScreen.kt    # Screen for editing user display name (incomplete)
│   │   │   └── HomeScreen.kt           # Main screen showing welcome message, recent notes, and navigation
│   │   └── note/
│   │       ├── AddNoteScreen.kt        # Screen to create or edit notes, includes tagging and formatting UI
│   │       └── ViewNoteScreen.kt       # Displays the content of a selected note in read-only format
│
│   ├── ui/
│   │   └── theme/
│   │       ├── Color.kt                # Defines app color scheme and Material3 theming
│   │       ├── Theme.kt                # Root Compose Material theme setup
│   │       └── Type.kt                 # Font and typography definitions
│
│   ├── viewmodel/
│   │   ├── AuthViewModel.kt            # Handles user authentication state and events (login, register, logout)
│   │   └── NotesViewModel.kt           # Manages Firestore note data, live state for note list, create/edit/delete logic
│
│   ├── MainActivity.kt                 # App's main entry point; hosts the Compose UI and calls AppNavigation
│   └── NotesApp.kt                     # Composable app container applying theme and surface scaffold



⚠️ Incomplete Features & Areas to Improve
👤 Add Google profile picture and display name to Profile screen
🛠 Implement working Edit Profile button
📈 Finish statistics calculations:
Most Active Day
Favorite Category based on tags
🏷 Organize notes by tag and make them searchable
💬 Add note sharing functionality
🧽 UI polish and animations for smoother transitions
🌐 Google Sign-In button branding (optional)
