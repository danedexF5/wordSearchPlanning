## Consider the /capabilities endpoint.

### At a minimum you must be able to generate puzzles with words hidden horizontally and vertically. 
What capabilities do you plan to support?
###What steps you think your code will have to take to return the JSON list of capabilities. 
Write this in English, as much as possible.
<br>
- Horizontal and vertical capabilities
<br>
- query from capabilties endpoint
<br>
- return board for the letters/words
<br>
- create the words, set the params


##Consider the /puzzle endpoint.

Think of two possible requests you might receive at the /capabilities endpoint. 
At least one of these must be a "difficult" request to fulfill. 
For example, a difficult request might be for a 30x30 puzzle containing 
20 words of 8 to 10 characters arrayed only at angles. Write out what these requests 
would look like in JSON. You can use an online tool to format this nicely.
{
    "width": 30,
    "height": 30,
    "words": 12,
    "minLength": 5,
    "maxLength": 10,
    "capabilities": ["angle"]
}

{
    "width": 10,
    "height": 10,
    "words": 5,
    "minLength": 3,
    "maxLength": 5,
    "capabilities": ["horizontal", "vertical"]
}



###For both of the requests you created, use a piece of paper and write a puzzle by hand. You can look up words in the /usr/share/dict/words file. Your hand-created puzzles must include words that intersect each other. Circle the words hidden your puzzle. Take a clear photo of the puzzle and include it in your document.
- (puzzle pic)


###As you create your puzzles by hand, write out EVERY SINGLE STEP you take. For example: 1. Determine the width and height of my puzzle. 2. Make a grid of corresponding height to hold my puzzle. 3. Determine the maximum and minimum length of words I can use. 4. Look in the words file and randomly pick a word that works 5. etc, etc, etc.

1. Width
2. Height
3. number of words
4. minimum length
5. maximum length
6. Capabilities
7. Make letters uppercase
8. Fill in words
9. Fill in empty spaces
10. Check for words crossing
11. Create methods and properties for Capabilities class
12. Create methods and properties for Puzzle class
13. Make sure the random generated words cannot exceed the walls

Refine your list of steps. This should be in sufficiently non-programmer terms that someone who had never before seen a word search puzzle could follow your instructions to create their very own puzzle.

###Using the information gleaned above, write about about the following:

**-How are you going to generate words for your puzzle?**
<br>
Create methods for the different directions the words can go in(horizontal, vertical, diag up, diag down).
<br>
**-How are you going to allow for words to intersect?**
<br>
Fill the random letters in after the words have been applied.
<br>
**-How are you going to structure the data that makes up a puzzle?**
<br>
We will form words that fit in the bounds by taking a dictionary.txt file turning it into a file we can read from. 
We'll then loop it so that it fits the spaces within our parameters.

###What else do you need to know or think about to successfully write your code?

I think a scanner will need to be utilized to read the numbers. We will also need to build the matrix using arrays.