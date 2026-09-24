# MODY-AI

MODY-AI is a Human-Computer Interaction university project developed through a semester-long, iterative design process. Its implemented high-fidelity prototype, **DrawTogether**, supports beginner and hobbyist artists as they upload drawings, revisit their progress, find inspiration, and reflect on their practice without external judgment.

## Project Overview

MODY-AI addresses the difficulty of maintaining a personal drawing practice and understanding progress over time. DrawTogether brings drawing uploads, local organization, progress browsing, inspiration categories, and prototype feedback into one mobile-oriented experience.

The project progressed from needfinding and paper prototypes to heuristic evaluation, medium-fidelity refinement, a high-fidelity Flutter prototype, and usability testing.

## HCI Design Process

### A1 - Needfinding

The repository contains needfinding deliverables, participant-research materials, consent documentation, and recorded sessions.

### A2 - Storyboard and Low-Fidelity Prototypes

The team produced mobile and tablet paper-prototype deliverables and storyboard material. The assignment document for this stage is also included.

### A3 - Heuristic Evaluation

The repository contains a heuristic-evaluation document and evaluator submissions. This stage provided the evaluation material later used during prototype refinement.

### A4 - Medium-to-High-Fidelity Refinement

Two evaluations were consolidated into heuristic violations with severity levels. The phone prototype was selected for refinement, with the Home and Progress screens developed in Figma as the main medium-fidelity focus.

### A5 - High-Fidelity Prototype and Usability Testing

The A5 submission includes a high-fidelity prototype document, a final report, a usability-testing protocol, and usability-testing reports. The implemented prototype is the Flutter project located in `A5/DrawTogether/draw_together`.

## Final Prototype: DrawTogether

The current Flutter prototype supports the following flows:

- Upload an image from the camera or gallery.
- Add drawing metadata including a required name, optional description, categories, and date.
- Store drawing metadata in a local SQLite database and copy selected images into application storage.
- Browse saved drawings in a Progress view.
- Search drawings by name, description, or category.
- Filter drawings by category.
- Open drawing details and zoom into drawing images.
- Browse bundled inspiration by category.
- Browse inspiration by difficulty level and open detailed inspiration views.
- View feedback-style messages while navigating between drawings.

Feedback is currently prototype behavior: the displayed messages are static and position-based rather than generated from an external service. The source includes feedback database tables and access methods, while the visible feedback flow currently uses local prototype text.

The application is local-first for the current prototype. It does not require a backend; image files are stored locally and their paths are recorded in the local database.

## Tech Stack

- Flutter
- Dart
- GoRouter for navigation
- Drift over SQLite for local typed database access
- `image_picker` for camera and gallery selection
- `path_provider` and `path` for local file storage
- Google Fonts
- Figma for the design and prototyping stage

Flutter dependencies are declared in [pubspec.yaml](A5/DrawTogether/draw_together/pubspec.yaml).

## Repository Structure

```text
.
├── A1/                              # Needfinding materials and research artifacts
├── A2/                              # Storyboard and mobile/tablet paper prototypes
├── A3/                              # Heuristic-evaluation materials
├── A4/                              # Medium-fidelity refinement and screenshots
├── A5/
│   ├── DrawTogether/
│   │   └── draw_together/           # Runnable Flutter application
│   ├── Final Report.pdf             # Final project report
│   ├── Test Protocol.pdf            # Usability-testing protocol
│   └── A5-high-fidelity-prototype.pdf
├── final-report-instructions.pdf    # Final-report instructions
└── README.md
```

The Flutter project is organized around `lib/app`, `lib/screens`, `lib/widgets`, and `lib/data/local`. Its bundled assets include inspiration images, progress seed images, and application artwork.

Research recordings, consent forms, and participant-related materials are intentionally not linked from this README.

## Running the Prototype

The runnable Flutter application is located at:

```text
A5/DrawTogether/draw_together
```

### Requirements

Before running the application, make sure the following are installed:

- Flutter SDK
- Dart SDK included with Flutter
- A supported Flutter target/device
- JDK 17 or newer when using the Android toolchain

You can verify your Flutter environment with:

```bash
flutter doctor
```

### Run the Application

Clone the repository and navigate to the Flutter project:

```bash
git clone <repository-url>
cd MODY-AI/A5/DrawTogether/draw_together
```

Install the project dependencies:

```bash
flutter pub get
```

Check the available devices:

```bash
flutter devices
```

Then run the application:

```bash
flutter run
```

If Flutter lists multiple devices, select the device on which you want to launch the prototype.

You can also explicitly select a target. For example, on Windows:

```bash
flutter run -d windows
```

The Windows build of the current prototype has been successfully built and launched.

### Java / Android Setup

If an Android build reports a Java or Gradle compatibility error, make sure Flutter is using **JDK 17 or newer**.

Check the active environment with:

```bash
flutter doctor -v
```

If Android Studio is installed, Flutter can be configured to use its bundled JDK. On Windows, for a standard Android Studio installation:

```bash
flutter config --jdk-dir "C:\Program Files\Android\Android Studio\jbr"
```

Then verify the configuration again:

```bash
flutter doctor -v
```

> The Android Studio path may be different depending on the local installation.

### Database Code Generation

Generated Drift database code is already included in the project. Regeneration is only necessary if the Drift schema is modified:

```bash
flutter pub run build_runner build --delete-conflicting-outputs
```

## Prototype Status and Limitations

DrawTogether is a university HCI prototype rather than a production release. Current prototype limitations include:

- Feedback is static and local rather than AI-generated or remotely retrieved.
- Seed data is enabled by default for demonstration.
- Image and database data are stored locally; no backend or synchronization service is included.
- The checked-in automated widget test should not be interpreted as application test coverage.
- Flutter platform scaffolding is included, but successful execution has not been verified on every generated platform target.

These limitations describe the current prototype scope and are not intended to represent the capabilities of a production version.

## Privacy

The repository contains research artifacts that may include participant-related information, consent documentation, recordings, external links, or personal data. These materials should not be redistributed or directly linked publicly without appropriate review, anonymization, and permission.

## Academic Context

MODY-AI was developed as a Human-Computer Interaction university project through an iterative process of research, prototyping, evaluation, refinement, implementation, and usability testing.

## Contributors

- Mohammadreza Babaei
- Ozgun Kocak
- Yusa Erguven
- Zuhal Didem Aytac