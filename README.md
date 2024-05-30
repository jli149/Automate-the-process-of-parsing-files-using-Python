# Automate-the-process-of-parsing-files-using-Python
This project involves using Python to work with a text file “allow_list.txt” that contains IP addresses that are allowed to access specific content at an organization. Additionally, the project requires writing an algorithm to automate the process of parsing files and to update the text file by removing IP addresses that shouldn’t have access.
Open the file that contains the allow list
 
In this step, I used ‘with’ statement and open function to open and read file “allow_list.txt” which is stored in variable ‘import_file’. The ‘open( )’ function requires two parameters. The first parameter is the file name, and the second indicates the action I want to perform with the file. ‘r’ indicates that I want to read the file. The output of the ‘open( )’ function is stored in variable ‘file’. 

Read the file contents 

I used ‘.read()’ method to convert the contents of the “allow_list.txt” file into a string and stored in variable ip_addresses for later use. 

Convert the string into a list 
Since string is immutable, I used ‘.split()’ method in this step to convert string to list and stored list in variable ‘ip_addresses’ in order to remove unwanted IP addresses later. 
Iterate through the remove list
 
In this step, I used ‘for loop’ to loop through every single element in the list ‘remove_list’. 
Remove IP addresses that are on the remove list
 

For every single element in the list ‘remove_list’, if the element is also in ‘ip_addresses’, then that element will be removed from list ip_addresses using ‘.remove()’
Update the file with the revised list of IP addresses 
 

In this step, ‘.join()’ method is used to convert list back to string since the variable  ‘ip_addresses’ must be in string format when used inside the ‘with’ statement to rewrite the file.
I used ‘.write’ method to update the file with revised IP addresses. 

Put it all into one function 
 
I created a function called ‘update_file( )’, in this case, it takes in two parameters, ‘import_file’ and ‘remove_list’. The body of the function consists code I wrote in previous steps. Then, I called the function ‘update_file( )’ and passed in two arguments “allow_list.txt” and ["192.168.25.60", "192.168.140.81", "192.168.203.198"]
Summary
In this project, the algorithm I wrote automates the process of removing unwanted IP addresses from the 'remove_list' in the text file 'allow_list.txt', which contains approved access IP addresses. This algorithm involves opening the file, converting its content to a string, and then converting it into a list, which is stored in the variable 'ip_addresses'. I then utilized a for loop to iterate through the 'remove_list' and applied the '.remove()' method to eliminate any IP address that matches an entry in 'ip_addresses'. Additionally, I used the '.join()' method to convert the list back to a string which updated the 'allow_list.txt' file with the revised list of IP addresses. This algorithm reduces the time required for manually deleting IP addresses one by one and is easily adaptable for similar tasks in the future.
