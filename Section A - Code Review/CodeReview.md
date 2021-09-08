
# Code Review

An SMS simulation Code Review

# Style

Your style of writing code is not efficient . The best way will be to create a class that will bundle the properties and
functionalities of your object . For example :

    #Create a class called SMS

    Class SMS :

        #Initialize or instatiate an object
        def __init__(self,text_message):
            self.text_message = text_message
            self.hasbeenread = False

        # Method manipulating a property to true  
        def mark_as_read(self):
            self.hasbeenread = True
    
Recall that in python we use indetation to highlight blocks of code . Your methods and property should be
within the body of a class . After your colol(:) we use whitespaces(4) for indetation.It is a way of telling a Python interpreter that the group of statements belongs to a particular block of code.

Your methods should include the key word 'self'
as an argument .With this keyword, you can access
the attributes and methods of the class in python.
It binds the attributes with the given arguments
For example :

    # Delete a text message using its index
    def remove(self,index):
        del self.inbox_folder[index]
        return 'Text deleted'


Dont forget to bundle all your methods and properties inside the body of the 
class paying special attention to indetation.

I suggest that you create a function for your SMS menu . Functions helps
us to modularize our code . It can look like this :


    # Menu for user interaction
    def menu():
        '''User Interface . If the user enters quit, the programs stops , 
        if read , texts messages are returned for user to read ,otherwise send
         a message to someone'''

        # So long as input is not quit keep going
        while userChoice != "quit":
            userChoice = raw_input("What would you like to do -
                                   read/send/quit?")
        
            if userChoice == "read":
                # Call function responsible for reading
                texts.read()
        
            elif userchoice == "send":
                # Call function that enable you to create and send email
                texts.send(adress,text_message)

            elif userchoice == "quit"
                print("Goodbye")
            
            else:
                print("Oops - incorrect input")

You seem to be  using multiple assignment at the beginnig of your code line
at line 1 . In python explicit code is better than implicit code . I suggest that
you separate your assignment for easy readability . The example below shows you how we assign instance variables .

    hasBeenRead = False  # Set hasBeenRead to False
    def __inti__(self,hasBeenRead,messageText,fromNumber):

        '''Initialize or construct an object '''

        self.hasBeenRead = hasBeenRead
        self.messageText = messageText
        self.fromNumber = fromNumber
           

Note !, this is how you Initialize your instance variables .    

## Documentation

Your code is not well documented . Its good practise to document your code . Use a # symbol followed by the 
statements , usually the statements explain your code , tells us how and in some cases why a certain code exist.
Doc strings are also crucial , put your statements within three qoutes like so '''Your statements should be here'''
, look at the code below . Example .

    class SMS :

    ''' The program simulates an SMS object , it performs the following functions
        : allows user to read an sms , write and send an sms , count the number of sms 
        within the inbox folder , delete an sms and mark a sms as sparm or as read .'''

        def count(self):
            # Return the number of sms in the inbox folder .
            return len(self.inbox_folder)


I suggest that you install flake8 for linting or make use of PEP8 so that you make use of python good's standards .

## Corretness and Efficiency .

Your code is not efficiently implemented . Create an SMS class , as explained above , a class is a blueprint that allows you
to construct as many 'SMS' objects as you can faster . Your solution will make it harder to do this and force you to be repetitive
when the need to create another SMS object arise . Remember to DRY in python , Do not Repeat Yourself .

The manner in which you assign instance variables is a bit flawed . Use self which represent
an instance of an class as shown above (line 3)

At line 11 . Your methods are outside a class . Functions defined within a class are called methods . These methods live inside a class . Make sure to bundle these 
methods within the body of a class . Use indetation for this purpose and adhere to Python's standards through Pep8 .

Your methods seem to be performing nothing . Make sure to write the logic of your code within the body of these methods . After creating your methods within the body of the class , create an object of class SMS like so

        # Create an SMS object
        obj = SMS(hasBeenRead,messageText,fromNumber)
        
        # Call the count method on object
        obj.count()

Realise that when creating an object , self is not included as a parameter . Putting it as an argument during your creation of a class
is sufficient .

