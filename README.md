# React Native useRef Bug: Unhandled Exception After Unmount

This repository demonstrates a common, yet subtle, bug in React Native applications involving the `useRef` hook.  The problem arises when a callback function associated with a ref is invoked *after* the component that holds that ref has been unmounted. This can lead to crashes or unpredictable behavior due to attempts to manipulate a no longer existing DOM element or component instance.

The `useRefBug.js` file contains the buggy code.  The `useRefSolution.js` file provides a solution which includes checking if the component is still mounted before proceeding.