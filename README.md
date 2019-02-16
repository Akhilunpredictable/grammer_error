# grammer_error
Main source is NPL.They have support for grammars that you can use to parse your sentence. You can define a grammar, or use one that is provided, along with a context-free parser. If the sentence parses, then it has valid grammar; if not, then it doesn't. These grammars may not have the widest coverage (eg, it might not know how to handle a word like StackOverflow), but this approach will allow you to say specifically what is valid or invalid in the grammar. Chapter 8 of the NLTK book covers parsing and should explain what you need to know.

An alternative would be to write a python interface to a wide-coverage parser (like the Stanford parser or C&C). These are statistical parsers that will be able to understand sentences even if they haven't seen all the words or all the grammatical constructions before. The downside is that sometimes the parser will still return a parse for a sentence with bad grammar because it will use the statistics to make the best guess possible.

So, it really depends on exactly what your goal is. If you want very precise control over what is considered grammatical, use a context-free parser with NLTK. If you want robustness and wide-coverage, use a statistical parser.

ii. Earley Parsing Algorithm
[2][8]Earley parsing algorithm is a hybrid type of parsing
algorithm. It combines the predictive rules of top-down
approach with robust bottom-up parsing. The algorithm was
designed for purpose of NLP. The algorithm maintains
dotted rules which help to keep a track of part of input,
which has already been seen before. Hence whenever any
predictions go wrong, then it doesn’t have start all over
again. Foe time complexities, unambiguous grammars are
O(n2
) time complex and ambiguous grammars are O(n3
)
time complex.
For the system here it is decided to opt for CYK algorithm
for its ease of use and in designing CFGs for English
grammar
D. Error Reporting
The error report module is designed for mapping parsing
errors to actual grammatical error. This component is
designed using Web-based technologies, which will help to
manipulate input text to display the incorrect part of
sentence, if any, to the user. Basically it is intended to
highlight error causing words. The reported errors will be
displayed to the user on a web page. 
