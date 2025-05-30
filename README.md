# MP-Exercise3

# Exercise 3: Bucket Collect Balls Game

## 🎯 Game Overview

Ball Catch Game is an arcade-style mobile game built with Flutter and the Flame game engine. Players control a bucket at the bottom of the screen to catch various types of falling balls, each with different point values. The objective is to reach 100 points while avoiding bombs and managing limited lives.

### Game Mechanics
- **Objective**: Score 100 points to win the game
- **Lives**: Start with 3 lives (❤️❤️❤️)
- **Controls**: Drag the bucket horizontally to catch falling balls
- **Difficulty**: Ball spawn rate increases as the game progresses

### Ball Types & Scoring
- **White Ball** (⚪): +5 points - Most common, slowest falling
- **Red Ball** (🔴): +10 points - Medium speed, moderate rarity
- **Gold Ball** (🟡): +15 points - Fastest falling, rare and valuable
- **Bomb** (💣): -30 points - Avoid these! They reduce your score significantly

### Game Rules
1. Catch balls by moving the bucket left and right
2. Missing any colored ball (not bombs) costs 1 life
3. Catching a bomb reduces your score by 30 points but doesn't cost a life
4. Game ends when you lose all 3 lives
5. Win by reaching 100 points
6. Ball spawn rate increases over time for added challenge

## 🚀 How to Run

### Prerequisites
- Flutter SDK (>=3.0.0)
- Dart SDK (>=3.0.0)
- Android Studio or VS Code with Flutter extensions
- Android device/emulator or iOS simulator

### Installation Steps
1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd ball_catch_game
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

### Build for Release
- **Android APK**: `flutter build apk`
- **Android App Bundle**: `flutter build appbundle`
- **iOS**: `flutter build ios`

## 📁 Project Structure

```
ball_catch_game/
├── lib/
│   ├── main.dart                 # App entry point and UI screens
│   ├── ball_catch_game.dart      # Core game logic and state management
│   ├── ball_components.dart      # Ball entities (White, Red, Gold, Bomb)
│   └── bucket_component.dart     # Player-controlled bucket component
├── android/                      # Android-specific files
├── ios/                         # iOS-specific files
├── test/                        # Unit and widget tests
├── pubspec.yaml                 # Dependencies and project configuration
└── README.md                    # This file
```

### Key Components

#### `main.dart`
- Contains the Flutter app structure and UI screens
- Manages game states (Start, Playing, Game Over, Victory)
- Handles screen overlays and user interface
- Provides restart functionality

#### `ball_catch_game.dart`
- Core game engine extending FlameGame
- Manages collision detection, scoring, and lives
- Controls ball spawning with dynamic difficulty scaling
- Handles pan gestures for bucket movement
- Implements win/lose conditions

#### `ball_components.dart`
- Defines abstract `BallComponent` class
- Implements four ball types with unique properties:
  - **WhiteBall**: Basic ball with black outline
  - **RedBall**: Higher value with gradient effect
  - **GoldBall**: Premium ball with sparkle effect
  - **BombBall**: Penalty item with fuse and emoji

#### `bucket_component.dart`
- Player-controlled game entity
- Handles horizontal movement within screen boundaries
- Manages collision detection with falling balls
- Visual representation of the catching mechanism

## 🛠️ Dependencies

The game uses the following key dependencies:

- **flutter**: Core Flutter framework
- **flame**: 2D game engine for Flutter (^1.15.0)
- **cupertino_icons**: iOS-style icons (^1.0.2)

Development dependencies:
- **flutter_test**: Testing framework
- **flutter_lints**: Code analysis and linting

## 🎮 How to Play

1. **Start Game**: Tap the "Start" button on the welcome screen
2. **Move Bucket**: Drag left and right to position your bucket
3. **Catch Balls**: Collect colored balls to gain points
4. **Avoid Bombs**: Don't catch bombs as they reduce your score
5. **Manage Lives**: Don't let colored balls fall past your bucket
6. **Reach Victory**: Score 100 points to win!

## 🏆 Game Features

- **Progressive Difficulty**: Ball spawn rate increases over time
- **Visual Feedback**: Smooth animations and particle effects
- **Responsive Controls**: Intuitive drag-to-move mechanics
- **Score Tracking**: Real-time score and lives display
- **Multiple Outcomes**: Victory and game over screens
- **Restart Capability**: Easy game reset functionality

## 🔧 Technical Implementation

- **Game Engine**: Built on Flame engine for 2D game development
- **Collision Detection**: Automatic collision handling between balls and bucket
- **State Management**: Game state handled through Flutter's setState
- **Performance**: Optimized for smooth 60fps gameplay
- **Cross-Platform**: Compatible with both Android and iOS devices

## 📱 System Requirements

- **Minimum Flutter Version**: 3.0.0
- **Minimum Dart Version**: 3.0.0
- **Android**: API level 16+ (Android 4.1+)
- **iOS**: iOS 9.0+
- **RAM**: 2GB minimum recommended
- **Storage**: 100MB for installation

---

**Have fun playing Ball Catch Game! 🎉**

*For issues or suggestions, please create an issue in the project repository.*
