import os
import time
def que(lst,dic):
    q=1
    count=0
    for keys in dic:
        print(keys)
        for i in lst[q-1]:
                print("     "+i)
        print("Enter the option: ")
        select=input()
        select=select.lower();
        if(select==dic.get(keys)):
                print("\t\t\tCorrect Answer\n")
                count+=1
        else:
                print("\t\t\tWrong Answer")
                print("\t\t\tCorrect Option:",dic.get(keys))
        q+=1
        x=input("\nPress enter key to go further- ")
        
        os.system("clear")
    print("\n\n\n\n\t\t\t\t\t\tPoints secured in Quiz: ",count,"/5")
    print("\n\t\t\t\t\t\tNumber of wrong answers: ",5-count)
    l=input("\n\tPress enter key to redirect to main page- ")
    os.system("clear")
def choose():
    print("\n\t\tChoose the level which you wanted to play: \n")
    print("1)Easy")
    print("2)Medium")
    print("3)Hard")
    chose=int(input("\t\tEnter the difficulty level number: " ))
    return chose
def datatypes_variables():
    ch=choose()
    dic={"1)Data types of x=3,y='s',z=4.5":"a","2)Built in data types of python are":"d","3)Data type of 1+2i:":"b",
         "4)Can a variable have same name as reserved words?":"b","5)Correct form of initializing a value to a variable":"c"}
    lst= [["a) int, string, float","b)double, char, float","c) float, int, double","d) int,char,float"],
         ["a)Sequential","b)Numbers, Sets","c)Boolean, dictionary","d)All of the above"],
         ["a) int","b) complex","c) either a or b","d) does not exist"],
		 ["a)True","b)False"],
         ["a)–p=9","b)break=7","c)	p=9","d)1p2=9"]]
    dic1={"what is the output of type(range(5)).":"c","What is the output of the following code "+
    "print(bool(0), bool(3.14159), bool(-3), bool(1.0+1j))":"d","Which of the following are immutable":"d",
    "What is the value of the  following arithemetic expression  5*2**10?":"b","which of the following is true?":"c"}
    lst1=[["a)int","b)list","c)range","d)none"],["a)False True False True","b)True True False True","c)True True False True"
            ,"d)False True True True"],["a)number","b)string","c)tuple","d)all of the above"],["a)100","b)5120","c)10000000000",
        "d)512"],["a)9%2=4","b)9/2=4","c)9//2=4","d)both b and c"]]
    dic2={"1) What is the result of round(0.5) – round(-0.5)? ":"b","2)What is the maximum possible length of an identifier?":"d",
            "3)What is the data type of print(type(0xFF))":"d","4)Scientific Notation for float number 0.0001234 is __":"b",
            "5. Which of these is not a core data type?":"d"}
    lst2=[["a)1.0","b)2.0","c) 0.0","d) None of the mentioned "],["a) 31 characters ","b) 63 characters","c) 79 characters"
    ,"d) none of the mentioned "],["a)number","b)hexint","c)hex","d)int"],["a)1234e-10","b)1.234e-04","c) 1234e-10","d)1234e-6"],
    ["a)Lists","b)Dictionary","c)Tuples","d)Class"]]
    os.system('clear') 
    if(ch==1):
        que(lst,dic)
    elif(ch==2):
        que(lst1,dic1)
    elif(ch==3):
        que(lst2,dic2)
def controlflow():
    ch=choose()
    dic={
    "1)correct syntax of writing ‘simple if’ statement is__":"c",
    "2)number of elif in a program is dependent on the _":"a",
    """3)
    Write the output of the following code:
    if True:
        print('Hello')
    else:
	    print('Bye')""":"b",
	"""4)What is the output of the following for loop and  range() function
                for num in range(-2,-5,-1):
                    print(num, end=", ")""":"d",
    """5)What is the output of the following nested loop

        numbers = [10, 20]
        items = ["Chair", "Table"]
        for x in numbers:
            for y in items:
                print(x, y)""":"a"}
    lst=[
    ["""a)if condition 
                statements""",
    """b)if (condition )
                    statements""",
    """c)if condition :
            statements""",
    """d)if condition - -
            statements"""],
    ["""a)number of conditions  to be checked""",
    """b)number of variables in a program""",
    """c). number of  loops in a program""",
    """d)none of the above """],
    ["""a)Bye""",
    """b)Hello""",
    """c)Bye
        Hello""",
    """d)Hello
        Bye"""],
    ["""a)-2, -1, -3, -4""",
    """b) -2, -1, 0, 1, 2, 3,""",
    """c) -2, -1, 0""",
    """d)-2, -3, -4,"""],
    ["""a)10 Chair
        10 Table
        20 Chair
        20 Table""",
    """b)10 Chair
        10 Table""",
    """c)10chair
         20 table""",
    """d)10chair
         20 chair
         10 table
         20 table"""]]
    dic1={
"""1)What is the output of the following range() function

            for num in range(2,-5,-1):
                print(num, end=", ")""":"c",
"""2)What is the output of the following loop

for l in 'Jhon':
   if l == 'o':
      pass
   print(l, end=", ")""":"b",
"""3)Select which is true for for loop""":"a",
"""4)What is the output of the following nested loop?

for num in range(10, 14):
   for i in range(2, num):
       if num%i == 1:
          print(num)
          break""":"a",
""" 5)What is the value of x after the following nested for loop completes its execution
x = 0
for i in range(10):
  for j in range(-1, -10, -1):
    x += 1
print(x)""":"b"}
    lst1=[["""a) 2, 1, 0""","""b)2, 1, 0, -1, -2, -3, -4, -5""","""c)2, 1, 0, -1, -2, -3, -4,""","""d) 2,-5,-1"""],
["""a) J, h, n,""","""b)J, h, o, n,""","""c) o""","""d)J,h"""],
["""a).Python’s for loop used to iterates over the items of list, tuple, dictionary, set, or string""",
"""b)else clause of for loop is executed when the loop terminates naturally""",
"""c)else clause of for loop is executed when the loop terminates abruptly""",
"""d)We use for loop when we want to perform a task indefinitely until a particular condition is met"""],
["""a)
10
11
12
13
""","""b)
11
13
""","""c)
10
12
""","""d).no output"""],
['a)99','b)90','c)100','d)9']]
    dict2={
"""1)what is the output of the following?
for i in "".join(reversed(list('wxyz'))):
	print(i,end="")""":"d",
"""2)what is the output of the following?
True=False
While True:
	print(True)
	Break""":"a",
"""3)what is the output of the following?
for i in range(int(float(‘inf))):
	print(i)""":"b",
	"""4)what is the output of the following?
for i  in [1, 2, 3, 4, 5]
	print(i,end=" ")
""":"c",
"""5)what is the output of the following?
i=0
while i<5:
	print(i)
	i+=1
	if i==3:
		break
else:	
	print(0)
""":"c"}
    lst2=[["""a)invalid syntax""","""b)wxyz""","""c)none of the mentioned""","""d)zyxw"""],
    ["""a)error""","""b)TRUE""","""c)none""","""d)FALSE"""],
    ["""a).0.0 0.1 0.2 0.3……""","""b)error""","""c)0 1 2 3…""","""d)0.0 1.0 2.0 3.0…."""],
    ["""a)5 3 1""","""b)1 3 5 ""","""c)1 2 3 4 5""","""d)none of the above"""],
    ["""a)FALSE""","""b)0 1 2 0""","""c)0 1 2""","""d)0 1"""]]
    os.system('clear') 
    if(ch==1):
        que(lst,dic)
    elif(ch==2):
        que(lst1,dic1)
    elif(ch==3):
        que(lst2,dict2)


def lists():
    ch=choose()
    dic={"1)what is a list?":"a","2)what type of data-type is list?":"c","3)What sort of bracket is for lists?":"d",
	     "4)Which of these is the correct code for creating a list of names?":"c","5)Which of the following statement is true?":"b"}
	     
    lst=[["a)used to store multiple items in a single variable","b)used to store multiple items in a single variable","c)used to store an single item in multiple variables","d)used to store mutliple items in multiple variables"],
	     ["a)numerical","b)non-sequential","c)sequential","d)boolean"],
	     ["a) () ","b) <> ","c) {} ","d)[] "],
	     ["a)nameList=John,Harry,Jesse,Harry","b)nameList=('John','Harry','Jesse','Harry')","c)nameList=['John','Harry','Jesse','Harry']","d)nameList=['John','Harry','Jesse','Harry']"],
		 ["a)Lists are immutable","b)Lists are mutable","c)Lists are both mutable and immutable","d)none of the above"]]
		 		 
    dic1={"1)Which of the following statements are true?":"b","2)list.split() method is for?":"d",
	      "3)The index() method in list returns?":"a","4)what are the methods of lists?":"d",
		  "5)Can you have lists inside of tuples and vice versa?":"a"}
    
    lst1=[["a)A Python list is immutable if every element in the list is immutable","b)A Python list is mutable if every element in the set is mutable","c)A Python list is immutable if every element in the tuple is mutable","d)A Python list is immutable"],
	      ["a)splits a string into a tuple","b)splits list into half","c)splits a sentence","d)splits a string into a list"],
	      ["a)The index of the given element in the list","b)The index of the first element in the list","c)The value of the element","d)none of the above"],
		  ["a)copy()" ,"b)insert()" ,"c)clear()","d)all of the above"],
		  ["a)Yes","b)No"]]
		  
    dic2={"1)What is the time complexity of insert for a list?":"b","2)Which operator is used to check if a list contains an element?":"d","3)Write syntax for slice:":"a","""4)\nlist1=[1, 2, 3]
list2=[4, 5, 6]
list(map(add,list1,list2)) \n what is the output for the following""":"a","5)Does a list need to be homogeneous?":"a"}
    
    lst2=[["a)O(1)","b)O(n)","c)O(n^2)","d)O(log n)"],
          ["a)present","b)is","c)yes","d)in"],
          ["a)slice(start, end)","b)slice(start)","c)slice(end,start)","d)slice(end)"],
          ["a)[5,7,9]","b)[1,2,3]","c)[4,5,6]","d)[9,7,5]"],
          ["a)no","b)yes"]]  
          
    os.system('clear') 
    if(ch==1):
        que(lst,dic)
    elif(ch==2):
        que(lst1,dic1)
    elif(ch==3):
        que(lst2,dic2)



def tup():
    ch=choose()
    dic={"1)A Python tuple can also be created without using parentheses":"a","2)Select true statements regarding the Python tuple":"d",
	     "3)How do you make a blank tuple?":"a","4)What are the methods available for tuple?":"b",
		 "5)\n  my_tuple = 3, 4.6,'dog'\n  print(my_tuple)\n  what is the output for the following":"c"}
		 
    lst=[["a)False","b)True"],
	    ["a)We can remove the item from tuple but we cannot update items of the tuple","b)We cannot delete the tuple","c)We cannot remove the items from the tuple","We cannot update items of the tuple."],
		["a)tuple=()","b)tuple=[]","c)tuple=0","d)tuple"],
		["a)copy() and clear()","b)count() and index()","c)pop() and remove()","d)insert() and append()"],
		["a) (my_tuple)","b) 3 4.6 god" ,"c) (3,4.6,'god')","d) no output"]] 
	
    dic1={"1)Suppose t=(1,2,4,3),t[1:-1] is .":"b","2)Suppose t = (1, 2, 4, 3, 8, 9), [t[i] for i in range(0, len(t), 2)] is ___.":"c","""3)\nWhat is the type of the following variable
aTuple = ("Orange")
print(type(aTuple))
""":"d","""4)my_tuple = ('p','r','o','g','r','a','m')
print(my_tuple[1:4])""":"b","5)For tuples which is correct?":"d"}
		 
    lst1=[["a)(1,2)","b)(2,4)","c)(4,3)","d)(2,3)"],
	    ["a)[1,2,4]","b)[2,3,9]","c)[1,4,8]","d)[3,8,9]"],
		["a)list","b)tuple","c)array","d)string"],
		["a)('p','r','o')","b)('r','o','g')","c)('o','g','r')","d)('g','o','r')"],
		["a)Tuples  are ordered,mutable and allow duplicates","b)Tuples  are in-ordered,immutable and doesnot allow duplicates","c)Tuples  are ordered,immutable and allow duplicates","d)Tuples  are ordered,immutable and doesnot allow duplicates"]]
		
    dic2={"""1)What is the method used in this program--
print((1, 2, 3) + (4, 5, 6))
Output: (1, 2, 3, 4, 5, 6)""":"d","""2)What is the output of the following
tuple1 = (1120, 'a')
print(max(tuple1))""":"a","""3)Find the output?
t1=(1,)*3
print(t1)
t1[0]=2
print(t1)""":"b","4)Which of these statement is correct for reversing tuple?":"a","""5)Find the output for the following:my_tuple = ('p', 'e', 'r', 'm', 'i', 't')
print(my_tuple[-1])
print(my_tuple[-6])""":"c"}
    lst2=[["a)addition","b)slicing","c)substraction","d)concatenation"],
          ["a)type error","b)a","c)1120","d)max(tuple1)"],
          ["a)t1","b)erroe","c)3","d)2"],
          ["a)tuple1 = tuple1[::-1]","b)tuple1(reverse)","c)reverse.tuple1"],
          ["a)'p' and 't'","b)'t' and 'e'","c)'t' and 'p'","d)'p' and 'i'",]]                                                                                                                                                                        
                                                                                                                                                                           
                                                                                                                                                                           
    os.system('clear') 
    if(ch==1):
        que(lst,dic)
    elif(ch==2):
        que(lst1,dic1)
    elif(ch==3):
        que(lst2,dic2)
    
def dictionary():
    ch=choose()
    dic={"1)What is the syntax of dictionary?":"a","""2)Suppose d = {“john”:40, 'peter':4}
    To obtain the number of entries in dictionary which command do we use?""":"b","""3)What will be the output of the following Python code snippet?
	d = {"john":40, "peter":45}
	print(d["john"])""":"a","4)Which of these about a dictionary is false?":"b","Which of the following isn’t true about dictionary keys?":"c"}

    lst=[["a)v={key:val}","b)v=(key:val)","c)v=[key:val]","d)all of the above"],["a) d.size()","b) len(d)","c) size(d)","d) d.len()"],["a)40","b) 45","c) 'john'","d) 'peter'"],["a) The values of a dictionary can be accessed using keys",
    "b) The keys of a dictionary can be accessed using values","c) Dictionaries aren’t ordered","d) Dictionaries are mutable"],
    ["a) More than one key isn’t allowed","b) Keys must be immutable","c) Keys must be integers","d) When duplicate keys encountered, the last assignment wins"]]
    dic1={"""What will be the output of the following Python code snippet?
	d1 = {"john":40, "peter":45}
	d2 = {"john":466, "peter":45}
	if d1 > d2:
		print('True')
	else:
		print('False')""":"c","""2)What will be the output of the following?\na={1:"A",2:"B",3:"C"}\na.setdefault(4)
    print(a)""":"d","3)What will be the output of the following Python code?\na={1:'A',2:'B',3:'C'}\na.clear()\nprint(a)":"d",
    "4) 13. What will be the output of the following Python code?\na={1:5,2:3,3:4}\nprint(a.pop(4,9))":"a",
    "5) What will be the output of the following Python code?\na=dict()\nprint(a[1])":"a"}
    lst1=[["a)True","b)False","c)error","d)None"],["a){ 1:'A',2:'B',3:'C'}","b){1:'A',2:'B'}","c){ 1:'A'}","d) { 1:'A',2:'B',3:'C',4:None}"],
    ['a) None','b) { None:None, None:None, None:None}','c) {1:None, 2:None, 3:None}','d) { }'],["a) 9","b) 3","c) Too many arguments for pop() method"
    ,"d) 4"],["a) An exception is thrown since the dictionary is empty","b) ' '","c) 1","d) 0"]]
    dict2={"1)Suppose d = {'john':40, 'peter':45}, to delete the entry for 'john' what command do we use?":"c","""2) What will be the output of the following Python code snippet?
    a={1:"A",2:"B",3:"C"}
    print(a.get(5,4))
    """:"c","""3)What will be the output of the following Python code?
    count={}
    count[(1,2,4)] = 5
    count[(4,2,1)] = 7
    count[(1,2)] = 6
    count[(4,2,1)] = 2
    tot = 0
    for i in count:
        tot=tot+count[i]
    print(len(count)+tot)
    """:"C","""4) What will be the output of the following Python code?
    a={}
    a[2]=1
    a[1]=[2,3,4]
    print(a[1][1])""":"b","""5)What will be the output of the following Python code?
    import collections
    b=dict()
    b=collections.defaultdict(lambda: 7)
    print(b[4])""":"d"}
    lst2=[["a) d.delete('john':40)","b) d.delete('john')","c) del d['john']","d) del d('john':40)"],["a) 1","b) A","c) 4","d) Invalid syntax for get method"],
    ["a) 25","b) 17","c) 16","d) Tuples can’t be made keys of a dictionary"],["a) [2,3,4]","b) 3","c) 2","d) An exception is thrown"],["a) 4","b) 0","c) An exception is thrown","d) 7"]]
    os.system('clear') 
    if(ch==1):
        que(lst,dic)
    elif(ch==2):
        que(lst1,dic1)
    elif(ch==3):
        que(lst2,dict2)
	    
print("\t\t\t\t___________________________________\n")
print("\t\t\t\t*******WELCOME TO QUIZ GAME********")
print("\t\t\t\t___________________________________")
x=input("\n\n\n\t\t\t\t\t   START THE QUIZ    ")
os.system('clear')
choice=1
while choice:
    print("\n\n\t\t\tTo start the quiz select any topic from the following :\n")
    print("1)Data types and variables")
    print("2)Control flow statements")
    print("3)List")
    print("4)Tuple")
    print("5)Dictionary")
    print("6)Exit")
    choice=int(input("\n\tEnter the chosen topic number: "))
    os.system("clear")
    if(choice==1):
        datatypes_variables()
    elif(choice==2):
        controlflow()
    elif(choice==3):
        lists()
    elif(choice==4):
        tup()
    elif(choice==5):
        dictionary()
    elif(choice==6):
        print("Thank you for playing")
        break




