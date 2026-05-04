# HelloMee

[HelloMee](https://hello-mee.vercel.app/) is an AI-powered language learning game where players help an alien character learn Earth languages through vocabulary acquisition.

## Overview

HelloMee is designed as a vocabulary learning game. Players interact with an alien character who is learning human language and culture. Through feeding text to the alien, players help it understand vocabulary and grammar. The game features a progression system where the alien levels up as it learns more words, and players can review learned vocabulary to reinforce their knowledge. The game also includes a postcard system that captures memorable moments from AI-generated content, creating a personalized learning journal.

Currently supported target languages: 
- English
- German
- French
- Spanish
- Swedish
- Japanese
- Chinese

## Playthrough

The game follows a structured progression system:

1. **Setup Phase**
   - Select username, target language, target level, and target country
   - Name your alien companion
     <img width="2553" height="1181" alt="图片" src="https://github.com/user-attachments/assets/314bd4f1-eb3d-4cb7-ad8d-f1967d40bc23" />
     <img width="2553" height="1188" alt="图片" src="https://github.com/user-attachments/assets/35a6aa54-2d59-40f8-92bd-c511224020c3" />

2. **Learning Loop**
   - Feed alien with text content
   - Memorize new words to Dictionary
   - Review previously learned vocabulary
   - Continue memorizing more words
   - If not sure what to do, check "About"
     <img width="2472" height="1176" alt="图片" src="https://github.com/user-attachments/assets/32320d31-ce43-475b-9ef0-bd03de378a15" />
     <img width="2472" height="1176" alt="图片" src="https://github.com/user-attachments/assets/270a1986-13c9-4e1d-8c60-0eaf1ed34b1b" />
     <img width="2469" height="1176" alt="图片" src="https://github.com/user-attachments/assets/da23f7b8-f26e-4f0d-9e1e-b564cf854923" />
     <img width="2475" height="1185" alt="图片" src="https://github.com/user-attachments/assets/ec14995a-dd8c-4878-8762-176609dc2061" />
     <img width="2559" height="1197" alt="图片" src="https://github.com/user-attachments/assets/ede30d63-1d82-4b20-80ca-eccd1df1dfcd" />

3. **Progression**
   - Reach level 2 to unlock postcards feature
   - Check collected postcards from AI interactions
   - Continue learning until reaching level 4
     <img width="2475" height="1188" alt="图片" src="https://github.com/user-attachments/assets/b4648203-bf58-4988-b61d-401c804f4343" />
     <img width="2475" height="1179" alt="图片" src="https://github.com/user-attachments/assets/f6cf1a05-5147-4a33-b410-a9e46705bde7" />

4. **Completion**
   - Receive a personalized thank you letter
   - Click "See you again" to clear game history and return to start
     <img width="2553" height="1188" alt="图片" src="https://github.com/user-attachments/assets/beccb964-cedf-4644-9deb-45071924424a" />
     <img width="2556" height="1188" alt="图片" src="https://github.com/user-attachments/assets/e97a4206-5cb0-4a50-9b52-ac4c17bfdf24" />

5. **Explore More Languages**
   - Pick another target language and speak to the alien — a whole new journey awaits you in that language:
    <img width="2559" height="1179" alt="图片" src="https://github.com/user-attachments/assets/993208be-501c-4718-a32d-895875507b2b" />
    <img width="2466" height="1179" alt="图片" src="https://github.com/user-attachments/assets/c21c6a1e-1f16-4c30-a687-503149887ad5" />
    <img width="2469" height="1176" alt="图片" src="https://github.com/user-attachments/assets/c7af0091-e8c6-4e23-bdf6-def9c4de1fd3" />





## Project Structure

```
src/
├── assets/                 # Static assets and text files
│   ├── system-prompt-level-1.txt    # AI system prompt for level 1
│   ├── system-prompt-level-2.txt    # AI system prompt for level 2
│   ├── system-prompt-level-3.txt    # AI system prompt for level 3
│   ├── system-prompt-review.txt     # AI system prompt for review
│   ├── system-prompt-congrats.txt   # AI system prompt for congratulations
│   ├── introduction.txt             # Introduction text
│   ├── sample-text.txt              # Sample text for feeding
│   ├── dummy-text.json              # Dummy text for different languages
│   ├── prompt-response-example.json # Example responses for different languages
│   └── logo.svg                     # Logo image
├── components/             # Vue components
│   ├── game/              # Game-related components
│   │   ├── CharacterStats.vue       # Character statistics display
│   │   ├── DictionaryModal.vue      # Dictionary modal for viewing learned words
│   │   ├── ProgressPanel.vue        # Progress panel showing level and stats
│   │   ├── StoryDisplay.vue         # Main story display component
│   │   ├── PostcardModal.vue        # Postcard modal for viewing collected moments
│   │   ├── Notification.vue         # Notification component
│   │   ├── LevelRequirements.vue    # Level requirements display
│   │   └── SeeYouAgainButton.vue    # "See you again" button component
│   ├── icons/             # Icon components
│   ├── HelloWorld.vue     # Hello world component
│   ├── TheWelcome.vue     # Welcome component
│   └── WelcomeItem.vue    # Welcome item component
├── router/                 # Router configuration
│   └── index.ts            # Router configuration file
├── stores/                 # Pinia state management
│   ├── gameStore.ts        # Main game state management
│   └── counter.ts          # Counter store (example)
├── views/                  # Page views
│   ├── StartView.vue       # Start page
│   ├── GameView.vue        # Main game page
│   ├── AboutView.vue       # About page
│   └── HomeView.vue        # Home page
├── App.vue                 # Root component
└── main.ts                 # Application entry point
```

## Features

1. **Multi-language Support** - Support for English, French, German, Spanish, Swedish, Japanese, and Chinese
2. **Character Creation System** - Create and customize your alien character
3. **Vocabulary Learning System** - Learn vocabulary through interactive stories
4. **RPG Elements** - Character leveling and progression system
5. **Dictionary Function** - View learned vocabulary
6. **Progress Tracking** - Monitor learning progress
7. **AI-Powered Content** - Dynamic story generation with DeepSeek API
8. **Postcard System** - Collect memorable moments from AI interactions
9. **Review System** - Reinforce learned vocabulary through spaced repetition
10. **Multiple Language Levels** - Different language levels for different languages (CEFR, JLPT, HSK)

## Tech Stack

- Vue 3 + TypeScript
- Vite Build Tool
- Vue Router for Navigation
- Pinia for State Management
- Tailwind CSS for Styling
- DeepSeek API for AI Content Generation

## Installation and Running

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Environment Variables Configuration

The project uses environment variables to store sensitive information such as API keys. To configure:

1. Copy the `.env.example` file and rename it to `.env`
2. Fill in your DeepSeek API Key in the `.env` file

```bash
cp .env.example .env
```

Note: The `.env` file has been added to `.gitignore` and will not be committed to the version control system.

## Component Descriptions

### Main View Components

1. **StartView.vue** - Start page where users can set their username, language preferences, and difficulty
2. **GameView.vue** - Main game interface containing all game functionality
3. **AboutView.vue** - About page with instructions and author information

### Game Components

1. **CharacterStats.vue** - Displays character status (health, level, etc.)
2. **StoryDisplay.vue** - Displays game story content and interactive vocabulary
3. **ProgressPanel.vue** - Displays progress information (current level, achievements, daily stats)
4. **DictionaryModal.vue** - Dictionary modal to view learned vocabulary
5. **PostcardModal.vue** - Postcard modal to view collected moments
6. **SeeYouAgainButton.vue** - "See you again" button for resetting the game
7. **LevelRequirements.vue** - Displays level requirements
8. **Notification.vue** - Notification component for displaying messages

## State Management

Pinia is used for state management. Game state is defined in `stores/gameStore.ts`:

- Character attributes
- Story content
- Vocabulary data
- Progress information
- Postcard collection
- Game settings (username, target language, etc.)

## Router Configuration

Routes are configured in `router/index.ts`:

- `/` - Start page
- `/game` - Main game page
- `/about` - About page

## Development Notes

1. All game components are located in the `src/components/game/` directory
2. View components are located in the `src/views/` directory
3. State management uses Pinia in the `src/stores/` directory
4. Router configuration is in the `src/router/` directory
5. Static assets are in the `public/assets/` directory
6. AI system prompts are in the `public/assets/` directory
7. Multi-language support is implemented through JSON files and dynamic content loading

## Important Notes

1. The project uses Tailwind CSS for styling
2. Fonts are loaded via Google Fonts
3. Data persistence uses localStorage
4. Responsive design adapts to different screen sizes
5. AI content generation powered by DeepSeek API
6. Multi-language support with dynamic content loading based on target language
7. Different language levels for different languages (CEFR for European languages, JLPT for Japanese, HSK for Chinese)
