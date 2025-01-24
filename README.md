# React 19 useEffect Double Run Bug

This repository demonstrates a bug encountered in React 19 where the `useEffect` hook appears to run twice on the initial render of a component. The component's functionality remains unaffected, but the duplicated console log indicates an unexpected behavior.

## Problem

The `useEffect` hook, intended to perform side effects after each render, executes twice during the initial mount in React 19. Subsequent updates trigger the `useEffect` only once as expected.

## Solution

The solution involves adding a dependency array to the `useEffect` hook that includes a flag to ensure the effect is only executed once after mount.  It's possible that the initial double run is due to a very specific component update or optimization that React 19 introduces and this solution avoids running useEffect prematurely.