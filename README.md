# React Native AsyncStorage: getItem returns null after setItem

This repository demonstrates a common issue in React Native when using AsyncStorage.  The problem occurs because AsyncStorage is asynchronous;  data isn't immediately available after using `setItem`.  This example shows the bug and a solution using promises or async/await.

## Bug Description

The bug is simple: `getItem` sometimes returns `null` or `undefined` immediately after `setItem`, even if `setItem` appears to have completed successfully. This is due to the asynchronous nature of AsyncStorage.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an emulator or device.
4. Observe the console logs, demonstrating the problem.

## Solution

The solution is to handle the asynchronous nature of AsyncStorage using promises or async/await.  This allows you to retrieve the data only after it has been successfully stored.