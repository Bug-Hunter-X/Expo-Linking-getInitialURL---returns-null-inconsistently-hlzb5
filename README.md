# Expo Linking.getInitialURL() Inconsistently Returns Null

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where the method sometimes returns `null` even when a deep link is successfully opened. This issue is more pronounced on Android devices.

## Problem
The `Linking.getInitialURL()` method is crucial for handling deep links, allowing apps to respond to specific URLs launched from external sources. However, it occasionally fails to return the expected URL, causing applications to behave unexpectedly.

## Steps to Reproduce
1. Clone this repository.
2. Run the app on both iOS and Android emulators/devices.
3. Try opening a deep link that should trigger a route change within the application.
4. Observe that on Android, the app may not correctly handle the deep link because `getInitialURL()` returns `null`.