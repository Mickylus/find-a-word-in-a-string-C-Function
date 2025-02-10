Main function code here

{

 	int findWord(char searched_string[],char word_to_search[]){
		int searched_string_lenght,word_to_search_lenght;
		// Inizalize the counters
		int j,i;
		// Gets the strings lenght
		searched_string_lenght = strlen(searched_string);
		word_to_search_lenght = strlen(word_to_search);
	 	// Searched string - word to search because there wouldn't be space to search
		for(i=0; i <= searched_string_lenght-word_to_search_lenght; i++){
			// Start the checking cycle
			for(j=0; j < word_to_search_lenght; j++){
				//Compare the string char by char
				// If two char don't match break the cycle
				if(searched_string[i+j] != word_to_search[j]){
					break;
				}
			}
			// If j got to the last char it means that the word was found and exit the function with code 1
			if(j == word_to_search_lenght){
				return 1;
			}
		}
		// If the word isnt found the function end with code 0
		return 0;
 	}
}
