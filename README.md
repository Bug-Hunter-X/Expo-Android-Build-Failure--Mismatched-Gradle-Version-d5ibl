# Expo Android Build Failure: Gradle Version Mismatch

This repository demonstrates a common, yet often difficult to diagnose, build error when using Expo CLI to build Android applications. The root cause is usually a discrepancy between the Gradle version specified in your project's `gradle-wrapper.properties` and the version expected by Expo Go.

The error messages generated are not always clear, leading to confusion and wasted time. This repo provides a reproducible example and a clear solution.

## Steps to Reproduce

1. Clone this repository.
2. Attempt to build the Android app using `expo build:android`. 
3. Observe the build failure.

## Solution

The solution involves ensuring your `gradle-wrapper.properties` file uses a compatible Gradle version.  Consult the Expo documentation for the latest recommended version. You might need to adjust the version in both `android/gradle/wrapper/gradle-wrapper.properties` and possibly `android/app/build.gradle` to align with the Gradle version accepted by Expo Go.  The solution provided in this repository shows the correct configuration.

## Additional Notes

This issue is often exacerbated by outdated dependencies. Keeping your project's dependencies up-to-date is crucial to avoid such conflicts.  Cleaning the build directory before rebuilding can also be helpful.