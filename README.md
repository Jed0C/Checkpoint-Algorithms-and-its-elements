ALGORITHM checkpoint
VAR
    charachter_counter: INTEGER :=0;  // character counter
    word_counter: INTEGER :=0;  //word counter
    vowel_counter: INTEGER :=0;     //vowel counter
    karakter : CHAR :='';       // declaring the input character
    word_flag : BOOLEAN := false;
BEGIN
    REPEAT
        //reading character by character
        READ(karakter)

        //checking if the character is a point "."
        IF (karakter = '.') THEN
            BREAK;
        END_IF

        //counting character by incrementing the counter by 1
        charachter_counter:= charachter_counter + 1;

        //checking if the character is a vowel (a,o,i,u,e,A,I,E,O,U)
        IF (karakter = 'a' or char='e' or char='i' or char='o' or char='u' or char='A' or char='E' or char='I' or char='O' or char='U') THEN
            vowel_counter := vowel_counter + 1;
        END_IF

        //counting words by checking the space between them
        IF ((karakter <> ' ') and (word_flag = false) ) THEN
            word_counter := word_counter + 1;
            word_flag := true;
        ELSE_IF ( karakter = ' ') THEN
            word_flag := false;
        END_IF
    
    UNTIL (karakter = '.')


    //writing the result
    WRITE("number of characters :",charachter_counter)
    WRITE("number of words :",word_counter)
    WRITE("number of vowels :",vowel_counter)
END
