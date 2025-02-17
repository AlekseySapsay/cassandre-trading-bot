---
lang: en-US
title: How to review code
description: How to review Cassandre code
---
# How to review code

## Common
* Variables in package order (batch, domain, dto, repository, service...), then strategy.

## Core code (not tests & not archetypes)
* Check class comment and see if there is a right usage of {@link}.
* Instance variable should have the same name as its class like: `UserService userService`.
* No new line between method start ({) and method end (}).
* When a variable represents an id, say it in the name like 'carId'.
* When a variable is DTO, say it in the name like `carDTO`.
* Check logs texts.
* No point at the end of logs texts.
* Add @ExcludeFromCoverageGeneratedReport when it's required.
* Use of Optional.ofNullable() instead of "if (x != null) return x.getAnyValue()".
* In services, first line of implementations is a log.

## Test code
* No comment on class.
* Test class with Package - Class `@DisplayName("Batch - Account flux")`.
* Method name and display name should declare with it tests `@DisplayName("Check received data")` 