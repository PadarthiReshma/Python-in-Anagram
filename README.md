# Python-in-Anagram

# Apporach-1

# function to check if two strings are
# anagram or not 
def check(s1, s2):
	
	# the sorted strings are checked 
	if(sorted(s1)== sorted(s2)):
		print("The strings are anagrams.") 
	else:
		print("The strings aren't anagrams.")		 
		
# driver code 
s1 ="listen"
s2 ="silent"
check(s1, s2)

# Apporach-2

#  To check if two strings are anagrams using sorted()

str1 = "Race"
str2 = "Care"

# convert both the strings into lowercase
str1 = str1.lower()
str2 = str2.lower()

# check if length is same
if(len(str1) == len(str2)):

    # sort the strings
    sorted_str1 = sorted(str1)
    sorted_str2 = sorted(str2)

    # if sorted char arrays are same
    if(sorted_str1 == sorted_str2):
        print(str1 + " and " + str2 + " are anagram.")
    else:
        print(str1 + " and " + str2 + " are not anagram.")

else:
    print(str1 + " and " + str2 + " are not anagram.")

#   Apporach-3

def anagramCheck2(str1,str2):  
    # Convert string into lists  
    list1 = list(str1)  
    list2 = list(str2)  
    # Sort the list value  
    list1.sort()  
    list2.sort()  
  
    position = 0  
    matches = True  
  
    while position < len(str1) and matches:  
        if list1[position]==list2[position]:  
            position = position + 1  
        else:  
            matches = False  
  
    return matches  
  
print(anagramCheck2('python','ythonp'))  

