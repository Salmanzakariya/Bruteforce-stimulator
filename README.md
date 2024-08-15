# Bruteforce-stimulator
# brute fore stimulation
import random
data_list="1234567890abcdefghijklmnopqrstuvwxyz" #creating data  for matching
chardata=list(data_list)   #  we casted data_list char to list

#Now creating a section for inserting password

password=str(input("Enter the password :")) 

#creating a while loop for matching password
preduction=""                      # first making the preduction section null
while(preduction != password):      #the condition for the loop is "preduction != password"/(for begginners :the reason we put != because the while loop only work when the password is not matched.when they matched it will stop).
    preduction = random.choices(chardata,k=len(password)) #matching with random numand char
    print(preduction)#printing the preduction password.
    preduction="".join(preduction)#joining the 2 string i the list to 1 .eg["1","1"]->11
    #its stops and goes to while condition and checks wether its true(match)or not.if its not it will goes till true.
    #once its true it true its print
print("THE password is ",preduction)
