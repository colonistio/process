# PR Review

Here are some guidelines to follow when you're reviewing code:

## General

- Never close someones PR, request them to do it.
- Never delete someones branch, request them to do it.
- Never edit or push to someones branch, request them to do the changes. In some scenarios you can do this like when it is a bottleneck.

## Reviewing code written in your ownership area (Example: Jeff commits in GameController)

- Main goal here is to enforce code maintainability. Code should be clean, understandable.
- Try to pinpoint risky spots that need unit tests.

## Reviewing code written outside someones ownership area: (Example: Goktug commits in client)

- We have multiple goals, make sure the PR is functionality correct, implementation correct, bug free and maintainable.  
- To make sure it is functionally correct, download branch, run the game, verify functionality. 
- To make sure it is implemented correctly, check architecture, imports, functions being used.
- To make sure it is bug free demand unit tests when appropriate. Note down for play testers to focus on this feature.
- If feature is in risk of a lot of bugs, push to onlinecatan so testers can try this in isolation.
- To make sure it is maintainable read every line, try to understand the flow and request changes.

## Merging Branches

- Squash Merge:
    - When a smaller PR is being merged into a master branch. Ex squash merge `jeff/adding-knight-logic` into `jeff/master-Cities-and-knights`
    - When a standalone PR is being merged directly into `development`. Ex squash merge `jeff/fix-longest-road-bug` into `development`
- Normal Merge:
    - When a multi-PR `master` branch is being merged into `development`. Ex normal merge `jeff/master-Cities-and-knights` into `development`
- These rules are being added to keep commit history clean while making it easy to revert PRs if needed
- More examples: https://prnt.sc/201291q https://github.com/colonistio/katan/pull/3649#issuecomment-779654090

## Source: 
- https://softwareengineering.stackexchange.com/questions/261801/how-to-deal-with-no-code-reviews-in-my-new-place-when-i-come-from-that-practice/261814
