# IP_Lookup
Implementation of IP lookup by binary search on length


!!!! FILES AND THEIR USAGE FOR PROGRAM EXECUTION!!!!
1) Steps to run and compile the program remains same as instructed with changes in file name.
2) Here for testing we are using Test_Table.txt as routing table to contain the prefixes and their corresponding portnums
3) Test_packets is the wireshark packet used to test if the lookup is working as expected
4) binary_search_by_legth_output is the png file showing the output for the test ran using test wireshark packets and test routing table

!!!!! EXPLAINATION OF CODE !!!!!!
1) Here the header file binarylength.h includes hash implemtation so as to create a hash table with prefix_length as its key and prefix and portnumber as its value.
2) Every time data is read from the Test_Tabe.txt its written in the corresponding key as defined by the prefix length in Test_Table.txt file.
3) Lookup involves masking address with different prefix length and then looking up in the hash table at the index which equals the prefix length. Depending on the result whether the required prefix value is matched or not matched the min and max prefix length is changed and required prefix length is calculated.