# ADHD Voice Assistant MVP Roadmap

## Project Overview

Building an ADHD-focused voice assistant that captures racing thoughts and manages multi-calendar scheduling. Starting with MVP for iOS 14+ (wide compatibility), then evolving to iOS 26 AI-powered features in v2.

## MVP Core Features (6-8 weeks)

### 1. Voice Thought Capture

- **iOS 14+ SFSpeechRecognizer** (maximum device compatibility)
- One-tap voice recording with automatic transcription
- Save thoughts as searchable text notes
- Tag thoughts by domain (work, personal, ideas, urgent)
- Export functionality (email, copy, share)

### 2. Multi-Calendar Integration

- **Google Calendar** (personal accounts)
- **Apple Calendar** (native EventKit)
- **Microsoft Outlook** (work accounts)
- Multiple accounts per provider support
- Unified calendar view across all connected accounts
- Smart calendar selection for event creation

### 3. Voice Calendar Intelligence

- Read appointments across all calendars with context
- “You have 9:30 AM doctor appointment at Sharp from personal calendar”
- Conflict detection across multiple calendars
- Natural language availability queries
- ADHD-friendly scheduling with automatic buffer time

### 4. Basic Thought-to-Event Creation

- Convert voice thoughts to calendar events
- Smart calendar suggestion based on content
- Automatic 15-minute buffer time addition
- Simple priority-based reminders

## Technical Stack

### Core Architecture

```
├── iOS 17+ target (Enhanced SFSpeechRecognizer)
├── SwiftUI + Core Data + CloudKit
├── EventBus Architecture (ADHD-specific)
├── District-based feature organization
│   ├── VoiceDistrict (speech capture)
│   ├── CalendarDistrict (multi-calendar)
│   └── IntelligenceDistrict (pattern detection)
├── Universal Calendar Manager
│   ├── Google Calendar API
│   ├── EventKit (Apple Calendar)
│   └── Microsoft Graph API
└── ADHD Intelligence Engine
    ├── Pattern Detection
    ├── Energy Tracking
    └── Gentle Interventions
```

### Dependencies

- Google Sign-In SDK
- Google Calendar API
- Microsoft Authentication Library (MSAL)
- EventKit (built-in iOS)

### Required Permissions

- Microphone access for voice capture
- Calendar access for event management
- Speech recognition for transcription

## User Experience Flow

### Onboarding (ADHD-friendly)

1. Welcome + core value proposition
1. Microphone permission request
1. Optional calendar connections (can skip)
1. First voice capture test
1. Success confirmation

### Daily Usage

1. **Thought Capture**: Tap → speak → automatic save
1. **Calendar Check**: “What do I have today?” → spoken summary
1. **Event Creation**: Voice thought → suggest calendar → create event
1. **Conflict Prevention**: Automatic detection across all calendars

## Development Timeline

### Week 1-2: Foundation

- Xcode project setup with iOS 14+ target
- Core Data model for thoughts and calendar accounts
- Basic SwiftUI interface structure
- SFSpeechRecognizer integration
- Google Calendar API authentication

### Week 3-4: Multi-Calendar System

- Universal Calendar Manager implementation
- Apple Calendar (EventKit) integration
- Microsoft Calendar authentication
- Unified event reading across providers
- Basic conflict detection

### Week 5-6: Voice Intelligence

- Calendar voice queries (“What’s next?”)
- Natural language event creation
- Thought-to-calendar conversion
- ADHD-friendly response formatting

### Week 7-8: Polish & Ship

- Error handling and edge cases
- ADHD-optimized UI/UX refinements
- Testing with real multi-calendar scenarios
- App Store submission preparation

## Success Metrics

- **Retention**: 40% users active after 7 days
- **Engagement**: Average 3+ thoughts captured per active day
- **Calendar Usage**: 30% of users create events from thoughts
- **Time to Value**: First successful voice capture within 2 minutes

## V2 Evolution Path (iOS 26)

- Foundation Models AI analysis
- SpeechAnalyzer for superior accuracy
- Advanced domain analysis (8 life areas)
- Professional help recommendations
- Business intelligence features
- Pattern recognition and insights

## Revenue Model

- **MVP**: Free core features
- **V2 Premium**: $2.99/month for AI insights
- **Business Features**: $9.99/month for professional tools

## Competitive Advantages

- **Multi-calendar support** (most apps only do one)
- **ADHD-specific design** (not adapted from neurotypical tools)
- **Voice-first interface** (optimal for racing ADHD thoughts)
- **Privacy-focused** (local processing, no cloud requirements)
- **Conflict prevention** (critical for ADHD scheduling)

## Key Implementation Notes

### ADHD-Specific Design Principles

- **Immediate value**: No complex setup required
- **Gentle interactions**: No overwhelming notifications
- **Forgiveness**: Easy to recover from mistakes
- **Flexibility**: Multiple ways to accomplish tasks
- **Context awareness**: Understand multi-calendar reality

### Technical Priorities

- **Reliability over features**: Core functionality must work perfectly
- **Performance**: Voice capture should be instant and accurate
- **Accessibility**: Support for various ADHD accommodations
- **Offline capability**: Core features work without internet

### Critical Success Factors

1. **Voice capture quality**: Must be better than built-in voice memos
1. **Calendar integration reliability**: Cannot miss or duplicate events
1. **Onboarding simplicity**: Users succeed within first 60 seconds
1. **Multi-calendar handling**: Seamless experience across providers

-----

## Ready to Build

This MVP proves the core hypothesis: Will ADHD users consistently capture thoughts via voice and create calendar events from them? Everything else in v2 builds on this foundation.

**Next step**: Create Xcode project and start with voice capture + local storage. Once that works reliably, add calendar integrations one by one.
