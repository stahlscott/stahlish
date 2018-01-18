---
title: 'Books: Clean Code, Chapters 5-?'
date: '2018-01-15'
tags:
  - books
  - clean code
published: false
---

### Chapter 5: Formatting

> Communicating is the professional developer's first order of business.

Profile of a product that is approximately 50k lines, comprised entirely of <200-500 line files.

Details should go from high-level at the top of the file to most detailed at the bottom of the file. Think of it like a newspaper article, with highlights and overview at the start and details at the end. But related concepts should be grouped in a class.

Whitespace & indentation are incredibly useful but should also be used in moderation. Paragraphs are easier than chapters. I've personally been burned by deploying a function that was perfect in every way except for a single missed indentation, which brought our customers down for a day. Probably would have been caught if I had broken the function up into smaller pieces.

### Chapter 6: Objects & Data Structures

Express data in abstract terms.

> Objects hide their data behind abstractions and expose functions that operate on that data. Data structures expose their data and have no meaningful functions.

OO & procedural/functional code are 'virtual opposites' in terms of what they do well vs poorly.

Avoid making hybrid objects/data structures. This seems like a point in favor of n-tier (service, dao, dto/data model). Keep your data models clean and drop all the complex methods into services.

### Chapter 7: Error Handling

TK
