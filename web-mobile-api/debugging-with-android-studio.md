# Debugging with Android Studio

**Read time:** 3 min

---

For Android app testing, first you have to connect your simulator or real device
to your Android Studio. This is done through ADB(Android Debug Bridge). 
More details can be found at their official website [Android Debug Bridge](https://developer.android.com/tools/adb).

We will discuss here two Android Studio tools that account for most
real debugging value — Logcat and the Layout Inspector. Exact menu
locations shift between Android Studio versions; the concepts below stay
stable regardless.

## [Logcat](https://developer.android.com/studio/debug/logcat) — the Android equivalent of browser Console + Network combined

Every log line from the app (and the OS) streams here — exceptions,
network calls (if the app logs them), custom debug output. The single
highest-value skill is **filtering effectively**: filtering by package
name (your app only, not OS noise), by log level (Error/Warning first
when triaging a crash), and by a specific tag if the app uses structured
logging.

**Practical habit:** when a tester reports "the app crashed" with no
other detail, the first move is always Logcat filtered to Errors for
that package — the stack trace is almost always sitting right there.

## [Layout Inspector](https://developer.android.com/studio/debug/layout-inspector) — for rendering/layout bugs specifically

Shows the actual rendered view hierarchy on a connected device/emulator
in real time — useful for the mobile equivalent of the web "is this a
rendering bug or a data bug" question: is a UI element missing because
it's not in the view hierarchy at all (a code/data bug) or because it's
present but invisible (a styling/layout bug)? Those are different bugs
with different owners, and Layout Inspector answers the question in
seconds instead of guessing.

## What to check before filing a "device-specific" bug

Before assuming a bug is genuinely device/OS-version-specific:
- Confirm the Android OS version and API level actually differ between
  the device that reproduces it and the one that doesn't
- Check Logcat on both for any difference in errors/warnings, not just
  the visible symptom
- Rule out a stale build/cache on one device before concluding it's a
  real platform difference — a mismatched build is a much more common
  cause than genuine OS-version behavior differences

## Best Practices

- Build a personal Logcat filter preset for "my app, errors and
  warnings only" — this single filter resolves a large share of "what
  actually happened" investigations
- Use Layout Inspector before filing a UI bug as "element missing" —
  confirm whether it's actually missing from the hierarchy or just
  visually hidden, since the report and the fix differ
- Keep in mind Android Studio's UI evolves between versions — if a
  described menu path doesn't match what you see, search current docs
  for the equivalent feature rather than assuming it was removed

For more information on debugging Android App - [Official Android Website](https://developer.android.com/studio/debug).

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [Web, Mobile & API Testing](./README.md)*
