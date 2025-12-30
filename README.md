# Exam Themes Frequency
Purpose:
Find frequencies and hottest themes of the greek final University Entrance exams for my students, for the course of Application development in a Programming Environment (ΑΕΠΠ). 

I [found](https://www.panellinies.net/%CE%B1%CE%B5%CF%80%CF%80-%CE%B1%CE%BD%CE%AC%CF%80%CF%84%CF%85%CE%BE%CE%B7-%CE%B5%CF%86%CE%B1%CF%81%CE%BC%CE%BF%CE%B3%CF%8E%CE%BD-%CF%83%CE%B5-%CF%80%CF%81%CE%BF%CE%B3%CF%81%CE%B1%CE%BC%CE%BC%CE%B1/) all the greek university entrance examinations for the above subject and I chose the newest 12 (2014-2025).

## Preprocecing of the files
- Copy each exam's context into a .txt file
- The exams questions are seperated in 4 Themes followed by an amount of excersises for each theme: 

| Θέμα n          | *Theme n*        |
|-----------------|-----------------|
| Εκφώνηση        | *Description*   |
| Άσκηση n1       | *Exercise n1*   |
| .               | *.*             |
| .               | *.*             |
| .               | *.*             |
| Άσκηση nk       | *Exercise nk*   |


For n in [A,C] , k in [1,~5]
- I broke each .txt into *Theme n* and *Excersise nk* pieces, using Regex. *Description* is optional, so I only kept *Themes* which were followed by some text
- All the above are added in a single python list

## Counting apperances

- I applied the deep learning model SentenceTransformer for semantic similarity on the list containing the excersises and themes
-Using cosine similarity and key words that match certain excersuses descriptions, I placed every excersise in one or more of the following clusters:
[matrices , lists_queue_stack_theory, graphs_theory, write_program, flowchart, fillin, subprograms, oop, matching same_structure, errors, write_theory] (or unknown if neither of the keywords are a match)
- I treated the *Excersise 1* of *Theme A* seperately, as it is always a True-False excersise and I wanted to see the context of each True False question seperately

## Final Product
Lastly, I plotted all the counts of each cluster in a bar graph, visualizing the most frequent themes



