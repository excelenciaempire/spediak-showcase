# Spediak client engineering

## Input and generation

The current main action sends the photo and notes directly to the statement-generation API. Audio transcription appends text to the notes before generation. The user can review and edit the resulting statement.

## Distinct outcomes

Media selection, recording, transcription, upload and generation have separate state. Saving the generated result is a separate API operation: a draft can be visible even if saving fails. A generated statement therefore does not establish a persisted history entry.

## Mobile and web

React Native and Expo share interface code while file handling, microphone permissions and recording differ by platform. Clerk supplies client authentication. Backend authorization, live generation and store distribution require their own runtime checks.

[Case overview](README.md)
