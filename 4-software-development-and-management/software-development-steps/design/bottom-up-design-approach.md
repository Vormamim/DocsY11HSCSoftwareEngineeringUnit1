---
icon: book-open
---

# Bottom-Up Design Approach

Bottom up program design starts with the component parts and repeatedly combines them to achieve the general concept.

## Advantage

* Create robust, reusable low-level utilities then decide how they will be put together to create high-level construct.

## Disadvantage

* The complete program does not exist without the addition of the last module such that testing of system-level functions is not possible during development.

## Example: Generating Quizzes

* Basic Elements: Question Model, Difficulty Level, Topic Filters
* Functional Module: Quiz Generation - selects questions based on specified criteria like difficulty level and topic.
* Integration into Major Function: Quiz Engine - uses the Quiz Generation module to create quizzes, tracks user answers, and calculates scores.
* Core Component Formation: The Quiz Engine is integrated with User Management and Results Analysis to form a comprehensive educational product.
