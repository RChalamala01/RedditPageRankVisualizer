# Reddit PageRank Visualizer

REPO DESCRIPTION:
The CS225 folder contains the code for PNGs, HSLApixels, RGB_HSL, and Animation (for our force-directed graph gif). The SpringEmbedder folder contains our code for a general force directed graph along with a spring embedded force directed graph which inherits from force directed graph. Our tests folder and util folder contain our necessary code for running and testing the test cases in test.cpp. Our documents folder contains files such as the proposal, the team contract, the development log, etc.
Preprocessing.py contains the code for processing the Stanford Reddit hyperlink dataset (without lengths) into a tsv file.
Graph.h and Graph.cpp contain the code for our directed graph structure which contains processing code (processes the tsv file), the subreddit nodes and edges, associated functions, and the pagerank algorithm. 
Pagerank.cpp contains code for running our pagerank algorithm and outputting the top 10 subreddit nodes by popularity.
Main.cpp contains the code for reading from the tsv file to process the nodes into the graph, running pagerank and printing the results (top ten), running BFS and creating a vector containing the traversal, printing an adjustable node of the bfs – along with its depth and a series of predecessors, essentially the shortest path from the starting node –, creating a springembedded force directed graph and writing it to test.png, and lastly code for the gif animation which is commented out (as it takes time to run).

COMMANDS TO RUN THE PROGRAM:
Run preprocessing.py to download and preprocess dataset.
Make pagerank then ./pagerank to run pagerank algorithm.
Make main then ./main to run pagerank, bfs, springembedded force directed graph, and animation (if you uncomment the code).
Make test and ./test to run the test cases.
The output locations for running these executables is the terminal; we also have gifs and pngs for the forcedirected graph.

TESTS:
Our tests/tests.cpp file contains our test cases which include BFS size test which checks if the size of the graph is the same as the BFS traversal vector size; a BFS duplicates test which checks if any of the nodes in the traversal are repeated; a pagerank normalized probabilities test which checks if the popularities of our ranked subreddits add up to 100%; a printrank nonexistent test which prints the popularity of a nonexistent subreddit; and a printrank existent test which prints the popularity of an existent subreddit.
