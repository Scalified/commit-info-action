# Commit Info GitHub Action

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/Scalified/commit-info-action/blob/master/LICENSE)
[![Release](https://img.shields.io/github/v/release/Scalified/commit-info-action?style=flat-square)](https://github.com/Scalified/commit-info-action/releases/latest)

## Overview

A simple GitHub Action to generate commit information in the following **JSON** format:

```json
{
   "hash": "a1b2c3d4e5f6g7h8i9j0klmnopqrstuvwx123456",
   "commitDate": "2025-08-14 13:45:02 +0300",
   "comment": "Fix: resolve config map replace issue",
   "buildDate": "2025-08-14 14:10:27 +0300"
}
```

> Uses [git-commit-info-json](https://gist.githubusercontent.com/vbaidak/2c700413c4862e7a92f366040f2ff3ea/raw/git-commit-info-json.sh) script

## Usage

```yaml
- name: Generate commit info
  uses: scalified/commit-info-action@v1
  with:
    file: version.json
    hash: a1b2c3d4
```

## Inputs

| Input  | Description                                      | Required | Default            |
|--------|--------------------------------------------------|----------|--------------------|
| `file` | Path to the file where commit info will be saved | No       | `""`               |
| `hash` | **Git** commit hash to generate information for  | No       | Latest commit hash |

## Outputs

| Output        | Description                                                   |
|---------------|---------------------------------------------------------------|
| `commit-info` | **Git** commit information                                    |
| `short-hash`  | Short version of the **Git** commit hash (first 7 characters) |

---

**Made with ❤️ by [Scalified](http://www.scalified.com)**
