---
title: We built a Custom Transport for Vercel's AI SDK
url: https://ably.com/blog/custom-transport-vercel-ai-sdk
date: '2026-05-13'
author: Zak Knill
feed_url: https://ably.com/blog/rss
---
The Vercel AI SDK's default transport is built for HTTP. That works until you need multi-device delivery, resumable streams, or more than one user in a conversation. We built a custom Ably transport for useChat, and hit the state machine assumptions it wasn't designed to handle.
