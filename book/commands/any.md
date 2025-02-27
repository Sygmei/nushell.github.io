---
title: any?
layout: command
version: 0.60.1
usage: |
  Tests if any element of the input matches a predicate.
---

# `{{ $frontmatter.title }}`

<div style='white-space: pre-wrap;'>{{ $frontmatter.usage }}</div>

## Signature

```> any? (predicate)```

## Parameters

 -  `predicate`: the predicate that must match

## Examples

Find if a service is not running
```shell
> echo [[status]; [UP] [DOWN] [UP]] | any? status == DOWN
```

Check if any of the values is odd
```shell
> echo [2 4 1 6 8] | any? ($it mod 2) == 1
```
