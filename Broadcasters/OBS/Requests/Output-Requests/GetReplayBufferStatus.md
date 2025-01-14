---
title: GetReplayBufferStatus
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-31T23:54:03.632Z
tags: 
editor: markdown
dateCreated: 2022-08-05T09:44:50.767Z
---

## Overview
Gets the status of the replay buffer output.

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputActive` | `Boolean`{.datatype} | Whether the output is active

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--1"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "GetReplayBufferStatus"
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#getreplaybufferstatus)
{.btn-grid .my-5}