# VoicePrint — Speech-to-Text Flutter App

A Flutter mobile app that transcribes live microphone speech to text, highlights
keywords, and copies the result to the clipboard.

## How it works

`lib/main.dart`:

1. Tapping the microphone button initializes the phone's native speech
   recognizer through the `speech_to_text` plugin and starts listening, with a
   glowing mic animation while active.
2. Recognized words stream into the display in large type.
3. A hardcoded keyword list (college-related words such as "exam",
   "professor", "resume") is highlighted in color via the `highlight_text`
   package.
4. The recognition confidence score is shown in the app bar; tapping the mic
   again stops listening.
5. A copy button places the full transcript on the clipboard.

Note: transcription is performed by the device's built-in speech recognition
(Android/iOS), not by a model in this repo. There is no training code and no
ML model files here.

## How to run

```bash
flutter pub get
flutter run
```

Requires a Flutter SDK and a physical device or emulator with microphone
support.

## Built with

Flutter/Dart; `speech_to_text`, `highlight_text`, `avatar_glow`, `clipboard`
packages.

## Known limitations

- Accuracy and language support depend entirely on the device's native speech
  recognition.
- The keyword highlight list is hardcoded; there is no settings screen to edit
  it.
- Transcripts are not saved — closing the app loses them.

## What was difficult

[Shreya to write — not obvious from the code.]
