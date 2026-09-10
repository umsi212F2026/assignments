# Questions you should be able to answer

Some of these will be fodder for class discussion. Others may show up on mini-quizzes.

**Working through these with your agent is not cheating. It is studying.** Ask it anything
you like about them. The answers still have to end up in your head, though, because that is where they
get checked.

Questions marked **(your submission)** are about your own files and results specifically. The
rest are about the analysis and could be asked of anyone.

---

## Knowing it is right without trusting the code

The three techniques, in the order you would actually reach for them.

### The smell test

1. If the "at least 50 ratings" filter were missing from task 1, what would the top of the list
   look like? How would you spot that from the output alone, without reading any code?
2. What average rating in a task 1 result would make you suspicious rather than pleased?
3. Task 2 counts only users who rated 25 or fewer movies. Before computing anything: roughly how
   many of the 610 users do you expect that to be? How could you check cheaply?
4. Are your top-rated movies films that anyone has heard of? If they were all obscure, would that be a cause for concern? Why or why not?
5. Name something that must be true of your results no matter what the data says. Could your code
   check it for you?
6. `movielens/README.txt` states its own totals. Did your code's counts agree with them? What
   would a disagreement have told you?
7. **(your submission)** Which result in your report are you least confident in? What would make
   you confident?

### Small datasets you can check by hand

8. **(your submission)** In `TEST-DATASETS.md` you claimed one of your datasets would catch a
   particular mistake. Pick that one and walk me through how it catches it.
9. **(your submission)** Did any of your datasets find a real problem in your code? Which one,
   and what was wrong?
10. **(your submission)** If you could keep only one of your artificial datasets for testing, which one, and why that one?
11. What mistake can you imagine that you could **not** build a dataset for?

### A second implementation

12. You wrote the JavaScript version in a fresh session. What kind of mistake does that catch that
    rewriting it in the same session would not? What kind does it still miss?
13. **(your submission)** Did your two implementations ever disagree? About what, and which one
    turned out to be right?
14. Why a different language, rather than a second Python version?

## Understanding what you computed

### Genres

15. Genres are stored as a single string, `Adventure|Animation|Children`. What is the most likely
    thing to get wrong here, and what would the answer look like if it happened?
16. Can one movie raise a user's genre count by more than one? Should it?
17. Thirty-four movies in this dataset carry the genre `(no genres listed)`. Did you handle it?
    Did handling it change your answer?
18. **(your submission)** Your answer says some user rated movies from N different genres. Pick
    that user, name their movies, and defend N by enumerating all the genres.

### Thresholds, and why they are there

19. "At least 50 ratings." Does a movie with exactly 50 count? How do you know your code agrees
    with your answer to that?
20. Why does task 2 have a threshold at all? What is the answer without it, and why is that
    answer uninteresting?
21. What does `movielens/README.txt` say about the smallest number of movies any user rated? What
    does that do to the meaning of task 2's threshold?

### Task 3, and your alternative measure

22. **(your submission)** What is your alternative measure, and what does it do that the naive
    count does not?
23. **(your submission)** Your alternative fixes a bias in the naive count. What is your alternative biased toward?
24. **(your submission)** How much do your two lists of pairs overlap? What does the amount of
    overlap tell you about your alternative measure?

### Reading the results

25. What does "broadest taste" actually measure here? Name something it misses.
26. Someone reads your report and asks "so what?" What is the most interesting thing in it, and
    why is it interesting?
