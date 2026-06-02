---
title: 'Engineering message appends for AI Transport: three vignettes'
url: https://ably.com/blog/engineering-message-appends-for-ai-transport-three-vignettes
date: '2026-05-06'
author: Simon Woolf
feed_url: https://ably.com/blog/rss
---
At Ably we recently shipped AI Transport, our drop-in transport layer for streaming LLM output over Ably channels, with all the resumability, multi-device continuity, and handover guarantees that implies.

One of the tricky things about token streaming from a pub/sub point of view is that while a model progressively emits fragments of text, those fragments logically all belong to a single message. You want to deliver them to the user live as they're produced, but for many other purposes you want
