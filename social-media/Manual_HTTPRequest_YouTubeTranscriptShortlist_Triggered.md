# Arcmira: YouTube Transcript Search

[Arcmira](https://arcmira.com) · [API docs](https://arcmira.com/docs) · [Original workflow](https://github.com/arcmira/integrations/tree/master/examples/n8n-source-shortlist)

Find up to three spoken passages about a topic in indexed YouTube videos. Keep timestamps, source links and coverage notes for editorial review. Uses only built-in n8n nodes and starts manually.

## Setup

1. Import [the workflow JSON](Manual_HTTPRequest_YouTubeTranscriptShortlist_Triggered.json) into n8n.
2. Create an **HTTP Bearer Auth** credential with your [Arcmira API key](https://arcmira.com/docs/authentication). Enter only the token, without a `Bearer ` prefix, and select it in **Search Arcmira**.
3. Set `topic`, `after` and `before` in **Search input**. Dates are UTC; `after` is inclusive and `before` exclusive. Choose dates your account can access.
4. Execute once and inspect **Build source shortlist**. Keep the requested/applied windows, `partial`, `search_index` and `note` alongside the results.

An Arcmira account is required. Limited free access and paid plans are available; see [usage and billing](https://arcmira.com/docs/usage-and-billing). Each manual execution makes one search request with `limit=3`. Errors stop execution. No retries, pagination, transcript requests, monitor writes or media downloads are configured.

## Evidence and limits

This JSON is byte-identical to the public distributed workflow. Its nodes, code and wiring ran on October 7, 2026 in n8n 2.41.3; packaging removed only the local workflow ID and empty pin/tag metadata. That run returned three passages and used zero measured credits. Its index reported `catching_up`. See the original [verification record](https://github.com/arcmira/integrations/blob/master/examples/n8n-source-shortlist/verification.json).

No new live run or browser-editor test was performed for this contribution. Results and coverage may change. Timestamps are navigation hints, not verified edit boundaries. Check the source, attribution and reuse rights before publishing; empty results do not prove absence.

## License

Copyright 2026 Arcmira. This workflow and its accompanying instructions retain [Apache-2.0](Manual_HTTPRequest_YouTubeTranscriptShortlist_Triggered.LICENSE). The collection's MIT license does not relicense these files or grant rights to third-party media or hosted-service access.
