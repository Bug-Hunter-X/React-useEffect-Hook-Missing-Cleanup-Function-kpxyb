# React useEffect Hook Missing Cleanup Function
This repository demonstrates a common React bug involving the `useEffect` hook. The bug occurs when a cleanup function is omitted from an effect, leading to potential memory leaks or unexpected behavior when the component unmounts.

## Bug Description
The provided `MyComponent` uses `useEffect` to log a message to the console when the component mounts. However, it's missing a cleanup function (returned from the effect). This can cause issues if the component mounts and unmounts frequently, potentially causing memory leaks or interfering with other lifecycle methods.

## Solution
The solution involves adding a return statement within the `useEffect` function. This return statement should contain a cleanup function that is executed when the component is unmounted. In this example, we are simply clearing the logged message. For more complex scenarios, this cleanup function might involve cancelling subscriptions, clearing intervals, or removing event listeners.