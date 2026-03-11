# Muzzle — Product Requirements Document

## Vision

**Muzzle** is an AI-powered audio privacy system that enables private voice interactions without being overheard.

**Tagline:** "Your AI hears you. Your neighbors can't."

## Problem Statement

- Users can't speak out loud in public spaces (offices, VA, hospitals, transit)
- Phone users are inconsiderate to those around them
- Bluetooth headphones leak audio to nearby listeners
- No existing solution provides **silent voice input** + **private transcription**
- Need for discreet voice interaction without bothering others

## Solution

Muzzle provides:
1. **Silent Voice Input** — Speak without others hearing (audio muzzled)
2. **Transcription** — Convert voice to text (cloud-based)
3. **AI Cleanup** — Make incomprehensible speech comprehensible
4. **Respectful** — You can use voice commands in public without bothering anyone
5. **Privacy First** — Audio muzzled locally; processing via secure APIs

---

## Release Strategy

### v1.0 (CURRENT FOCUS)
**Static site MVP — Get it out the door.**

- [x] Landing page (Astro)
- [x] Dark blue gradient design
- [x] Core messaging
- [x] CTA button
- [ ] Responsive finalization
- ❌ NO server-side models
- ❌ NO backend
- ❌ NO Bluetooth/audio features yet

**Goal:** Ship a clean, minimal landing page. Iterate based on feedback.

### B1 (Phase 2 — Full Product)
**Audio privacy + transcription system.**

Features:
- [ ] Bluetooth headphone pairing
- [ ] Audio capture & muzzling (silence output)
- [ ] Cloud transcription (Whisper, Google Speech-to-Text, etc.)
- [ ] Web dashboard (blue theme)
- [ ] Raw transcription storage

**Scope:** Audio privacy + transcription. No on-device AI models (Pico/Nano too small for complexity).

### Phase 3 (Future)
**AI-cleaned transcription pipeline.**

Features:
- [ ] Raw transcription (from voice-to-text)
- [ ] AI-cleaned version (makes incomprehensible speech comprehensible)
- [ ] Both versions available to user
- [ ] Voice commands & response generation
- [ ] Custom AI personalities

**Note:** Requires server-side model inference. Defer until after B1.

---

## Technical Stack

### v1.0
- **Frontend:** Astro (static site)
- **Design:** Dark blue gradient, minimal
- **Hosting:** Vercel (or similar)
- **No backend, no models**

### B1+
- **Frontend:** Astro + React (blue theme)
- **Backend:** Node.js / Python
- **Audio:** Web Audio API, Bluetooth API
- **Transcription:** Cloud API (Whisper, Google Speech-to-Text, etc.)
- **Database:** SQLite (local)

### Phase 3+
- **AI:** Cloud APIs for transcription cleanup (not local models)

---

## Success Metrics

### v1.0
- [ ] Landing page live and responsive
- [ ] Clear messaging on product positioning
- [ ] CTA button functional

### B1
- [ ] Audio muzzling works (neighbors can't hear)
- [ ] Transcription accuracy > 95%
- [ ] Response latency < 2 seconds
- [ ] User satisfaction > 4.5/5

---

## Timeline

- **v1.0 (NOW):** Static site, ship it
- **B1 (Later):** Audio + transcription features
- **Phase 3 (Future):** AI cleanup pipeline

---

## Philosophy

**Keep it simple. Ship it. Iterate.**

- v1.0: Static site only. No over-engineering.
- B1: Add features only when needed.
- Phase 3: Transcription cleanup is a nice-to-have, not a blocker.

---

**Created:** 2026-03-11  
**Last Updated:** 2026-03-11  
**Status:** v1.0 in development  
**Lead:** Paul Vudmaska
