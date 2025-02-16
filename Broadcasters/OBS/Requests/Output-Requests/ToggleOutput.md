---
title: ToggleOutput
description: OBS Studio Requests Reference (v5)
published: true
date: 2022-08-31T23:52:11.723Z
tags: 
editor: markdown
dateCreated: 2022-08-05T14:42:22.870Z
---

## Overview
Toggles the status of an output.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`outputName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Output name

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.outputActive` | `Boolean`{.datatype} | Whether the output is active

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--4"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json
{
  "requestType": "ToggleOutput",
  "requestData": {
    "outputName": ""
  }
}
```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#toggleoutput)
{.btn-grid .my-5}