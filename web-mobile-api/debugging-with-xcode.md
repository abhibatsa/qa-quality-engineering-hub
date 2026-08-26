# Debugging with Xcode

**Read time:** 3 min

---

For iOS app testing, device logs and Instruments cover most real
debugging needs. As with Android Studio, exact UI locations shift
between Xcode versions — the underlying concepts and workflow stay stable.

## Device Console / Logs — the iOS equivalent of Logcat

Streams system and app-level log output from a connected device or
simulator. Same core skill as Android's Logcat: **filtering effectively**
— by process (your app specifically), and by looking for crash logs and
errors first when triaging a reported issue.

**Practical habit:** for a reported crash, the device log (or a
generated crash report/symbolicated stack trace) is the first place to
look — same discipline as checking Logcat first on Android, different
tool, same underlying instinct.

**Using macOS Console App:**
This approach captures full system-level events, background activity, 
and unified os_log outputs.

1. Connect your iOS device to your Mac using a USB cable.
2. Unlock your iPhone/iPad and tap Trust if the "Trust This Computer" prompt appears.
3. Open the Console app on your Mac (Press Cmd + Space, type "Console", and hit Enter).
4. In the left sidebar, click on your iOS Device under the Devices section.
5. Click Start (or "Start streaming") in the top toolbar to begin reading the log feed.
6. Crucial Step: Go to the top menu bar, select Action, and check both Include Info Messages and Include Debug Messages.
If you skip this, Apple hides standard application logs by default.

// Reproduce your issue, use the top-right Search bar to filter by your app's name or process, and copy/paste the entries into a text editor to save them. //

## Instruments — for performance and resource-usage investigation

A profiling toolset for deeper investigation beyond "what happened" into
"why is this slow/using too much memory/draining battery" — Time
Profiler (CPU usage over time), Allocations (memory usage), Energy Log
(battery impact). Most QA testers won't live in Instruments daily, but
knowing it exists and what category of problem it solves is what lets
you correctly route a "the app feels slow" report to the right
investigation tool instead of guessing from the UI alone.

## Simulator vs. real device, iOS-specific considerations

Same general trade-off as covered in
[Mobile App Automation & Testing](./mobile-app-automation-and-testing.md),
with an iOS-specific note: certain capabilities (camera, certain
biometric flows, precise performance/battery characteristics) genuinely
require real-device testing — the Simulator approximates but doesn't
fully replicate real hardware for these categories.

## Best Practices

- Check device logs / crash reports before speculating about a crash's
  cause — same "logs first" discipline as Android, this resolves most
  "why did this crash" questions quickly
- Know Instruments exists as the right tool for performance-category
  reports specifically, even if you don't use it daily — routing a report
  to the right investigation tool is itself a real skill
- Same version-drift caution as Android Studio — if a described menu
  path doesn't match current Xcode, search current docs for the
  equivalent rather than assuming the feature disappeared

For more information on debugging - [XCode/iOS Debugging](https://developer.apple.com/documentation/xcode/debugging)

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [Web, Mobile & API Testing](./README.md)*
