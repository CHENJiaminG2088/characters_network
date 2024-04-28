## Report for fanfiction data collection, sample article preprocessing.

This report addresses the current situation regarding:
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

## Brief introduction of the baby network:(base on article An Unlikely Comfort)
![image](https://github.com/CHENJiaminG2088/characters_network/blob/main/screenshot_193815.png)
In this network, orange represents women and purple represents men. The vertex size is the number of times the character's name appears in the article. The weight of the edge represents the number of times two character names appear together at a particular length of text. As we can see from the diagram, if the central character is judged by the number of connected edges, then columbia is the central character of this article. If the central character is judged by the total number of occurrences, then Riff Raff is the central character.

## Introduction of the files:
1.Character name recognition and count.ipynb: Code for counting appearances of characters' names and co-occurrence within a certain text window size.  
2.booknlp_10_Rocky.ipynb: Code for processing ten articles using BookNLP.  
3.output_Ao3_10: The output of using BookNLP for ten articles.    
4.edges_An_Unlikely_Comfor.csv: The edge file contains the ID of the person's name, and the weight is the number of times the two persona names appear together within a specific text length.  
5.nodes_An_Unlikely_Comfor：The node file contains the name and ID of the character, and the "count" is the total number of times the name of the character appears in the text.


## Next steps:
1.Categorize articles by topic, e.g. by their topic, or sentiment tags, and then build a network of people under specific categories.  
2.Consider multiple articles with the same character name as nodes, and edges represent the co-occurrence of characters with the same name in different stories.

