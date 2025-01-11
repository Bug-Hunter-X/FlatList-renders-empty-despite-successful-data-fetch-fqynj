# React Native FlatList rendering issue

This repository demonstrates a common issue in React Native where a FlatList component renders empty despite successfully fetching data from an API.  The problem lies in the implementation of the `keyExtractor` function, which is crucial for FlatList's efficient rendering.

## Problem

The provided `bug.js` file contains a component that fetches data from a mock API and attempts to render it using a FlatList.  The FlatList remains empty even if the data fetch is successful. This is because the `keyExtractor` is using the index, which is not guaranteed to be unique if the data array is modified.

## Solution

The `bugSolution.js` file provides a corrected implementation.  A proper unique key is extracted from each item in the data array, resolving the rendering problem.

## How to reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.

Observe the behavior of the FlatList in both `bug.js` and `bugSolution.js` to understand the difference.
