ADHDVoiceAssistant (iOS 17+)
├── EventBus/
│   ├── ADHDEventBus (central nervous system)
│   ├── Events/ (ADHD-specific event types)
│   │   ├── VoiceCaptureStarted
│   │   ├── VoiceCaptureCompleted  
│   │   ├── ADHDPatternDetected
│   │   ├── CalendarEventSuggested
│   │   └── CelebrationTriggered
│   └── Districts/ (feature modules)
│       ├── VoiceDistrict
│       ├── CalendarDistrict
│       └── IntelligenceDistrict
├── Features/
│   ├── Voice/ (speech capture + transcription)
│   ├── Calendar/ (multi-provider integration)
│   └── Intelligence/ (ADHD pattern detection)
├── Core/
│   ├── Storage/ (Core Data + CloudKit)
│   ├── Authentication/ (OAuth for calendars)
│   └── Networking/ (API integrations)
└── UI/
    ├── SwiftUI Views (ADHD-optimized)
    └── Accessibility Components
