# Engineering walkthrough

## Human review between model steps

The inspected client separates the image/context input, preliminary description and final statement request. It exposes an editable preliminary description before the next request. That review boundary matters: an image interpretation should not silently become an asserted final finding.

## Multiple interaction states

Image selection, microphone permission, recording, transcription, upload and generation have different outcomes. The client tracks these states and user-visible errors rather than treating them as a single button response. UI state alone does not prove that retries, persistence or backend recovery are correct.

## Mobile and web boundaries

React Native and Expo provide shared interface code while platform checks, media permissions and file handling remain explicit concerns. The repository also contains SOP and statement-history routes, authentication dependencies and subscription integration. Dependency presence is not proof of successful payment processing or a completed store release.

## What I can discuss

The observation-to-draft flow, review before generation, media permissions, state management and integration boundaries. Runtime correctness, accessibility and backend authorization require checks beyond this source review.

[Back to the case](README.md)
