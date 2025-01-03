# React Native `onLayout` Event Bug

This repository demonstrates a common issue encountered when using the `onLayout` event in React Native.  The problem arises from race conditions and inconsistencies when attempting to obtain layout dimensions before the component has fully measured itself, often leading to inaccurate or undefined values. This repository shows the problematic code and a solution demonstrating more robust techniques for handling `onLayout` events.

## Problem Description

The provided example illustrates a scenario where obtaining dimensions from `onLayout` before the layout is fully calculated results in incorrect values being stored in the component's state. This can manifest as components rendering in the wrong locations, unexpected sizes, or even infinite render loops.  The challenge lies in ensuring that the layout calculations are completed before relying on the dimensions.