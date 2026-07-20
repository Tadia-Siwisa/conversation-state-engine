# conversation-state-engine
A Conversation State Engine (CSE) that introduces a conversational state layer between audio perception and LLM reasoning for multi-speaker voice AI.

# Conversation State Engine (CSE)

## Problem
Current voice assistants understand what is being said, but they do not explicitly maintain the state of a multi-speaker conversation. As new participants join, interrupt, or leave, conversational context and speaker attribution become difficult to manage.

## Solution
The Conversation State Engine (CSE) introduces a missing orchestration layer between Audio Perception and the Large Language Model (LLM). Rather than sending raw observations directly to the LLM, the CSE maintains the current conversation state and provides the LLM with a structured representation of the conversation before reasoning occurs.

## Architecture
Voice Input

↓

Audio Perception

↓

State Observations

↓

Conversation State Engine (CSE)

↓

Conversation State

↓

GPT / LLM

↓

Voice Output

## MVP

The first prototype demonstrates:

- Detect a new speaker entering a conversation
- Create and update conversation state
- Verify a new participant
- Resume the original conversation
- Maintain speaker attribution throughout the interaction

## Why this matters

## Future Work
- Multi-modal perception (vision, text, sensors)
- Persistent participant memory
- Emotion-aware conversation state
- Cross-device shared conversation state
- Distributed conversation orchestration
