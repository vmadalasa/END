### Problem Statement

1. Write a function using only list filter lambda that can tell whether a number is a Fibonacci number or not. You can use a pre-calculated list/dict to store fab numbers till 10000  
2. Using list comprehension (and zip/lambda/etc if required) write an expression that:  
    a. add 2 iterables a and b such that a is even and b is odd  
    b. strips every vowel from a string provided (tsai>>ts)  
    c. acts like a ReLU function for a 1D array  
    d. acts like a sigmoid function for a 1D array  
    e. takes a small character string and shifts all characters by 5 (handle boundary conditions) tsai>>yxfn  
3. A list comprehension expression that takes a ~200 word paragraph, and checks whether it has any of the swear words mentioned in https://github.com/RobertJGabriel/Google-profanity-words/blob/master/list.txt  
4. Using reduce function:  
    a. add only even numbers in a list  
    b. find the biggest character in a string (printable ascii characters)  
    c. adds every 3rd number in a list  
5. Using randint, random.choice and list comprehensions, write an expression that generates 15 random KADDAADDDD number plates, where KA is fixed, D stands for a digit, and A stands for Capital alphabets. 10<< DD <<99 & 1000<< DDDD <<9999  
6. Write the above again from scratch where KA can be changed to DL, and 1000/9999 ranges can be provided. Now use a partial function such that 1000/9999 are hardcoded, but KA can be provided  

### Implementation
##### Function for Ques. 1
**fab_checker:** This function checks if the number provided is a number in Fibonacci series. The input should be a positive integer less than 10,000. The function returns True or False indicating whether a the number provided is a number in Fibonacci series.  


##### Function for Ques. 2
**add_iter_even_odd:** This function adds 2 iterables a and b such that a is even and b is odd. The input should be a list of numbers. The function returns list with addition as per the above mentioned rule.  

**vowel_remover:** This function strips every vowel from a string provided. The input should be any string. The function returns string without any vowels.  

**relu:** This function that applies ReLU function to each elements of the provided list. The input should be a list of numbers. The function returns list with ReLU output for each of the elements of the list.  

**sigmoid:** This function that applies Sigmoid function to each elements of the provided list. The input should be a list of numbers. The function returns list with Sigmoid output for each of the elements of the list.  

**char_shifter:** This function shifts all characters by 5 for a string provided. The input should be any string. The function returns string with all characters shifted by 5.  

##### Function for Ques. 3
**profanity_checker:** This function checks whether it has any of the swear words mentioned in 'resources/profane_words.txt'. The input should be any paragraph as a single string. The function returns True or False indicating whether there is profanity in the paragraph.  

##### Function for Ques. 4
**even_adder:** This function that adds only the even numbers in the provided list. The input should be a list of numbers. The function returns sum of even numbers in the provided list.  

**vowel_remover:** This function strips every vowel from a string provided. The input should be any string. The function returns string without any vowels.  

**biggest_character:** This function finds the biggest character in a string (printable ascii characters). The input should be a string containing printable ascii characters. The function returns the biggest character in the provided string.  

**alt_adder:** This function that adds every 3rd number in the provided list. The input should be a list of numbers. The function returns sum of all (n+1)th numbers in the provided list where n is an even integer greater than zero.  

##### Function for Ques. 5
**num_plate_generator:** This function that generates 15 random number plates starting with KA (for Karnataka). The function does not take any input. The function returns list of 15 random number plates starting with KA.  

##### Function for Ques. 6
**num_plate_generator_2:** This function that generates 15 random number plates for the state code provided and the vehicle number between the range provided.  
The function takes 3 inputs:
- num_start: The least number allowed as vehicle number.  
- num_end: The highest number allowed as vehicle number.  
- state_code: Code of the state for which the number plate is to be generated.  
The function returns list of 15 random number plates based on the inputs.  
e.g. KA01HT2873

**num_plate_generator_3:** This function implements partial function on num_plate_generator_2. This function generates 15 random number plates for the state code provided and the vehicle number between the range provided.  
The function takes 1 input:
- state_code: Code of the state for which the number plate is to be generated.  
The function returns list of 15 random number plates based on the inputs.  
e.g. UK07AB4570
