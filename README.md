# Expo Camera: Inconsistent onBarCodeScanned Callback

This repository demonstrates a bug encountered when using the Expo `Camera` component's `onBarCodeScanned` prop. The callback function is not consistently triggered, leading to unreliable barcode scanning.

## Bug Description

The `onBarCodeScanned` function, intended to handle scanned barcodes, intermittently fails to execute.  This occurs across different devices and scenarios, making the barcode scanning functionality unreliable.  The barcode may be correctly scanned visually, but the data is not passed to the application.

## How to Reproduce

1. Clone this repository.
2. Run the `bug.js` example using Expo Go or a similar Expo development environment.
3. Scan a barcode using the app. Note that the `console.log` statement within the `handleBarCodeScanned` function may not print data consistently, despite successful barcode recognition by the camera.

## Solution

The provided `bugSolution.js` shows a possible workaround.  This might not be applicable in all scenarios and may need further optimization depending on specific use cases and Expo versions.

## Possible Causes

* Issues with Expo's camera implementation related to barcode scanning.
* Race conditions or timing issues within the app's logic related to the camera usage.
* Conflicts between the camera component and other library usages.

This report aims to highlight the inconsistency and provide a potential workaround.  A comprehensive fix likely requires addressing the root cause within the Expo Camera implementation.