## Report for novel data collection, sample novel preprocessing.

## This report addresses the current situation regarding:
1.The results of using BookNLP to extract named entities.
2.Counting characters' co-occurrence based on the occurrence of names within a certain window size.
3.Interpretation of the baby network.
## Collecting data
1. Type "the rocky horror picture show" into the search bar, and 758 results appear.
2. Select 10 random articles from the above results and download them in pdf format.

## procesing data:
1. Use Python to convert PDF to txt format.
2. Use booknlp to process the article: In this step, I am currently trying to process one of the articles, and the following content is related to processing this article
3. Use booknlp to extract a series of files and store them in the output file
4. Then use the code that extracts the name of the character and counts the number of occurrences to extract the name of the character in this article and the number of occurrences
5. I manually enter the name into the code that calculates the co-occurrence, and get the number of times the two names co-occur within a certain text length.

6. Convert the result into files of nodes and edges.
I try to use the name of the character as the node, and the co-occurrence of the two names as the edge, and the weight of the edge is the number of times the two names appear together within a certain text limit in the article.

## the baby network of one article:

## Introduction of the files:
1.Character name recognition and count.ipynb: Code for counting appearances of characters' names and co-occurrence within a certain text window size.  
2.booknlp_10_Rocky.ipynb: Code for processing ten articles using BookNLP. 
3.output_Ao3_10: The output of using BookNLP for ten articles.  
4.edges_An_Unlikely_Comfor.csv: The edge file contains the ID of the person's name, and the weight is the number of times the two persona names appear together within a specific text length.  
5.nodes_An_Unlikely_Comfor：The node file contains the name and ID of the character, and the "count" is the total number of times the name of the character appears in the text.


## next steps
1.Resolved the import issue of edge files
2.Consider multiple articles with the same character name as nodes, and edges represent the co-occurrence of characters with the same name in different stories.
