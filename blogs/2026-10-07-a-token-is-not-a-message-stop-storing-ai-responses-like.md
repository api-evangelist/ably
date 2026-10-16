---
title: "A token is not a message: stop storing AI responses like event logs"
url: "https://ably.com/blog/store-streamed-ai-responses"
date: "2026-10-07"
author: "Madeleine Quinn"
feed_url: "https://voltaire.ably.com/blog/rss.xml"
---
A model streams tokens, but a user reads a message. Store the tokens instead of the message, and every client that joins mid-response has to rebuild the response.
