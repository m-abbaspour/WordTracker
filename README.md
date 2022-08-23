# WordTracker
WordTracker reads text files and collects and stores all the unique words it finds 
	in those files. The BST created and tested in the utilities package will store 
	information from multiple text files. It will also keep track of each occurrence of 
	a word in a file and the line on which it was found in that file. This information 
	will be stored in a list for each word object stored in the BST. The program will 
	also produce output, specified by the user at command line, to generate reports using 
	a variety of iterators built into the BST.
	The BST created will be stored in a binary file "repository.ser". Every time the program 
	executes, it will check if the binary file (repository.ser) exists, and if so, restores 
	the words tree. The results of the scanning the next file are inserted in the appropriate 
	nodes of the tree. Therefore, repository.ser will contain all words occurred in all files 
	scanned with the meta information about those word locations.The repository.ser file will 
	be saved wherever the Wordtracker.jar file is saved.
  

  ## Execusion:
To run this program use the following format in the command prompt:

	java -jar WordTracker.jar <input.txt> -pf/-pl/-po [-f <output.txt>]
  
  <b>Notes: </b>
 <ol> 
 <li> `< input.txt>` is the path and filename of the text file to be processed by the WordTracker program </li>

<li>3 mutually exclusive options at command line:</li>

<ul>
			<li> -pf to print in alphabetic order all words along with the corresponding
			  list of files in which the words occur. </li>
			<li> -pl to print in alphabetic order all words along with the corresponding 
			  list of files and numbers of the lines in which the word occur. </li>
			<li> -po to print in alphabetic order all words along with the corresponding 
			  list of files, numbers of the lines in which the word occur and the 
			  frequency of occurrence of the words. </li>
</ul>

<li>Optional argument to redirect of the report in the previous step to the path and 
		  filename specified in `< output.txt>` </li>
<li>Users can provide arguments in any order they would like (The output file will 
		  be the one that is provided after the -f argument)</li>
</ol>
 
--------------

Created: August 2022

-------------------
Known deficiencies:
- If the file has been analyzed once, it will not ne analyzed again under the same name
- Names including dashes will not be read as one word
