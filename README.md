# InfinitiveQuestions
This is a simple bash program that guesses the animal (or, actually a general object, depends on how you define an animal) you have in mind, adapted from a course project of CSC209.
It does not doing any prediction, instead it learns from every failure and get the exact answer.
The idea is somewhat like the decision tree in ML.

USAGE
1. run the program with "sh better_animal database"
2. there you go.

FEATURES
Taking the inspration of decision tree in ML, the program guesses the animal user has in mind by asking yes-no questions. Unlike the concept of decision tree, it will make a guess at some point (when the program feel like the given info is clear enough). Once it gets the answer it will exit; otherwise user will be asked for what exactly they have in mind and an extra question (with a key) to identify it, then exit.

If you put enough time mess aroung with it, it gets more and more knowledgable & makes guesses closer to the expectation. lim_{time->infinity} questions = InfinitiveQuestions...???

Any of Y/y/N/n/Yes/yes/No/no is an acceptable answer input to the yes-no questions.

The small improvement free the requirement of an exisisting well-structured database. Any directory can now be passed in as an db argument, and it works as the program is learning from a new start.

BOUNDARIES
As for now it only accepts yes-no questions.
By default, on a fresh start it will ask if your animal have in mind is "Doge".

Database
The database follows the (binary) tree structure. Each subdir of a (sub)dir in database will either contains: a file called "name", a file called "question" + a subdir called "yes"/"no" or both of the subdirs.
The "question" file has a yes-no function. (technically it can be any questions, but the program only accepts y/n as answer for now)
The "name" file contains exactly a word/phrase of an animal (or a general object, again, depends on what you'd call an animal)
The sub-directories "yes" and "no" are the decision based on the answers.

AUTHORS
- Zelin Tan
