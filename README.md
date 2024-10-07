# File-Handling
# #open file and store file object in a variable
# file = open('Codingal.txt')

# # read the contents of file
# print(file.read())

# #close the file
# file.close()

# #open the file in read mode file in written mode
# file_write =open('Codingal.txt','r')
# print("File in Read Mode-")
# print(file_read.read())
# file_read.close()

# #opem the file in written mode
# file_write = open('Codingal.txt','w')
# #write in the file
# file_write.write("File in written mode...")
# file_write.write("Hi! I am Penguin. I am 1yr. old")
# file_write.close()

# #open the file in append mode
# file_append = open('Codingal.txt','a')
# # append in the file
# file_append.write("\n File in append mode....")
# file_append.write("Hi! I am Penguin,. I am 1yr. old")
# file_append.close()

# Program to count number of lines in this file
#Opening a file 
# file = open("Codingal.txt","r")
# Counter = 0

# #reading from file
# Content = file.read()
# #splitting contentinto lines
# #and storing them in a list
# CoList = Content.split("\n")

# for i in CoList:
#   if i:
#     Counter = 1
    
#   print("This is the number of lines in the file")
#   print('Counter')
# Program to append contents of file in another file

# entering the file names
firstfile = input("Enter the name of first file ")
secondfile = input("Enter the name of second file ")

# opening both files in read only mode to read initial contents
f1 = open(firstfile, 'r')
f2 = open(secondfile, 'r')

# printing the contens of the file before appending
print('content of first file before appending -\n', f1.read())
print('content of second file before appending - \n', f2.read())

# closing the files
f1.close()
f2.close()

# opening first file in append mode and second file in read mode
f1 = open(firstfile, 'a+')
f2 = open(secondfile, 'r')

# appending the contents of the second file to the first file
f1.write(f2.read())

# relocating the cursor of the files at the beginning
f1.seek(0)
f2.seek(0)

# printing the contents of the files after appendng
print('content of first file after appending - \n', f1.read())
print('content of second file after appending - \n', f2.read())

# closing the files
f1.close()
f2.close()
