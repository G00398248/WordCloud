# WordCloudSteps to run the project:

1. Open command prompt and point to the directory where the project jar is saved.
2. From the command line, run the command: java -cp ./wcloud.jar ie.gmit.dip.Runner

Features:

1. The entire project is packed in a package ie.gmit.dip
2. A menu driven UI is presented to the user with a suite of choices as follows:
- Read input as a file or from a URL
- Enter file path or file name (the program will search for file in current directory in this case)
- Maximum words to be displayed in the wordcloud
- File name of the wordcloud png to be saved
3. Functionality when input is a:
- File: Read the file contents with file parser with necessary IO exception handling
- URL: Read the URL contents with HTML parsing and write these contents in a file, read this file as in file input functionality
4. A hashmap which saves a word and the frequency with which it occurs in the content. Dupliction of words or keys in the hashmap is prevented by converting words to lowercase.
5. Only words which are not present in the ignorewords.txt are added in the hashmap. Words in ignorewords.txt are excluded from the wordcloud
6. Essential additional files like the ignorewords.txt are saved in the resources directory and referenced as a stream
7. The hashmap is sorted in descending order by frequency and the words in the wordcloud are drawn in a similar order with the most frequent words drawn on the top followed by the less frequent words as one moves to the bottom of the word cloud
8. A super class WordStyle is created which is extended by three subclasses to controll the properties of the words to be drawn in the wordcloud. These properties include the font style, color and fontsize of the word.
9. The positioning of the words in the wordcloud i.e. the x and y cordinates are calculated for dynamic placement of words.
10. All static methods are written in the Utilities.java file stating the time complexities.
11. The programs are Javadoc commented and all supporting files for the ame can be found in the docs folder
12. The UML diagram attached outlines the structure of the classes used in the program
13. The source code can be found in the src folder
