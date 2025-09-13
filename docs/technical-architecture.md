# Technical Architecture

## MVP Architecture (iOS 14+)


ADHD Voice Assistant
├── Core/
│   ├── EventBus (ADHD-specific event processing)
│   ├── VoiceCapture (SFSpeechRecognizer wrapper)
│   └── DataManager (Core Data + CloudKit)
├── Providers/
│   ├── GoogleCalendarProvider
│   ├── AppleCalendarProvider (EventKit)
│   └── MicrosoftCalendarProvider
├── Features/
│   ├── ThoughtCapture/
│   ├── CalendarIntelligence/
│   └── VoiceAssistant/
└── UI/
├── SwiftUI Views
└── ADHD-optimized components


## Key Components

### Universal Calendar Manager
- Protocol-based provider system
- Unified event model across providers
- Intelligent calendar selection
- Conflict detection across all calendars

### Voice Processing Pipeline
- SFSpeechRecognizer for transcription
- Natural language processing for intent
- Context-aware response generation
- ADHD-friendly error handling

### EventBus System
- Priority-based event processing
- ADHD-specific event types
- Comprehensive logging for patterns
- Future-proof for AI integration

## Data Models

### Core Entities
- `ThoughtCapture`: Voice recordings + transcriptions
- `CalendarEvent`: Unified event across providers
- `CalendarAccount`: Provider credentials + preferences
- `UserPreferences`: ADHD-specific customizations

### Relationships
- Thoughts can generate multiple calendar events
- Events link back to source thoughts
- Accounts have multiple calendars
- Users have multiple accounts per provider

## Privacy Architecture
- Local Core Data storage
- Encrypted credential storage
- Optional CloudKit sync
- No unnecessary cloud dependencies

## Future Evolution (v2)
- iOS 26 Foundation Models integration
- SpeechAnalyzer for enhanced accuracy
- Advanced AI pattern recognition
- Business intelligence features
