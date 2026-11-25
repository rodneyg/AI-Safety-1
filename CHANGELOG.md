# Changelog

Changes merged into this repository. Deployment patches are applied separately.

## 2026-11-25

- Added a [chat draft patch](deployment-fixes/README.md#t-11044-chat-draft-preservation) that clears the message box as soon as a message is sent, so text typed while the demo prepares its reply stays for the next send. [PR #6](https://github.com/rodneyg/AI-Safety-1/pull/6)

## 2026-11-21

- Added a [chat accessibility patch](deployment-fixes/README.md#t-10390-chat-accessibility) that gives the Send button a screen-reader label, removes an information button with no action, and improves avatar text contrast. [PR #4](https://github.com/rodneyg/AI-Safety-1/pull/4)

## 2026-11-20

- Added a [deployment patch](deployment-fixes/README.md) that gives the demo a descriptive browser tab title and page description, and lets direct requests for personal data trigger simulated verification on the first message, and raises the Next.js dependency from 15.2.8 to 15.5.29. [PR #1](https://github.com/rodneyg/AI-Safety-1/pull/1)
- Added a follow-up deployment patch so **Use Alternative** fills the chat input with the suggested rewrite for review before sending. The button is hidden when there is no rewrite, and a rewrite of a leading question now reads "what evidence supports or challenges the claim that ..." instead of "what do you think about ...". [PR #2](https://github.com/rodneyg/AI-Safety-1/pull/2)
