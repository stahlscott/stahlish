---
title: "Books Clean Code 3"
date: 2018-01-21
tags: 
  - books
  - clean code
published: false
---

### Chapter 9: Unit Tests

The essentials of TDD:

> **First Law:** You may not write production code until you have written a failing unit test.

> **Second Law:** You may not write more of a unit test than is sufficient to fail, and not compiling is failing.

> **Third Law:** You may not write more production code than is sufficient to pass the currently failing test.

The problem is that this massive amount of unit testing can be just as bad as no tests if the tests themselves are not written cleanly, and we tend to look at test code as good if it passes regardless of its structure. The tests will change as we write more code, so you're creating more tech debt by writing dirty test code.

> Test code is just as important as production code.

I agree with this:

> Readability is perhaps even more important in unit tests than it is in production code.

Very important to follow an explicit, clean, readable pattern, without any shortcuts. I like to use the following Arrange/Act/Assert pattern:
1) Arrange: stage data & set expected result variables
2) Act: execute the production code we're testing
3) Assert: run your assertions (Hamcrest++) against your expectations

This should make any test code I write simple for the reader to understand and modify to their needs. If the arrange step is repeated across methods, extract that to a helper. Easy and clear. This is also similar to Given/When/Then.

... as I continue one page further, they describe this exact thing as Build/Operate/Check. My name is catchier though. But they do show code I would describe as "fine" and refactor it with explicit, expressive helper methods to make it even clearer. I will consider doing this in the future.

> Test a single concept in each test function.

They recommend this over "one assert per function" which I agree with. Sometimes it makes more sense, to me, to have several asserts to test all angles of the same concept. One assert per function is overkill.

Summary concept: **F.I.R.S.T**

* **Fast** Tests should run quickly. This translates to more unit tests, more mocking.
* **Independent** Test should not depend on each other; they should be able to run in any random order and pass.
* **Repeatable** Tests should be able to run in any environment with the same results.
* **Self-Validating** Tests should either pass or fail, not output to a log and require manual checking.
* **Timely** The tests should be written just before the production code that makes them pass

> If you let your tests rot, then your code will rot too.

### Chapter 10: Classes

TK
