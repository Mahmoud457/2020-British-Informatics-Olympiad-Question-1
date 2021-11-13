import string 
import random

def checkPat(string):
  if len(string) < 2:
    return True
  for x in range(1, len(string)+1):
    left = string[0:x]
    right = string[x:len(string)]
    
    reverseLeft = left[::-1]
    reverseRight = right[::-1]
    TRight = False
    TLeft = False
    if test(left, right):
      if len(reverseLeft) == 1:
        TLeft = True
      if len(reverseRight) == 1:
        TRight = True 
      
      if TLeft and TRight:
        return True 
      for y in range(1, len(reverseLeft)+1):
        reverseLeft_left = reverseLeft[0:y]
        reverseLeft_right = reverseRight[y:len(reverseLeft)]
       
        if len(reverseLeft) == 2:
          reverseLeft_left = reverseLeft[0]
          reverseLeft_right = reverseLeft[1]
        
        if test(reverseLeft_left, reverseLeft_right):
         
          TLeft = True
           
        if TLeft == True:
          
          for z in range(1, len(reverseRight)+1):
            reverseRight_left = reverseRight[0:z]
            reverseRight_right = reverseRight[z:len(reverseRight)]
            
            if len(reverseRight) == 1:
              return True
            if len(reverseRight) == 2:
              reverseRight_left = reverseRight[0]
              reverseRight_right = reverseRight[1]
            if test(reverseRight_left, reverseRight_right):
              TRight = True
            
            if TRight == True:
              return True 


  
      





def test(left, right):
  alphabet = string.ascii_uppercase
  
  if len(left) >= 1 and len(right) >= 1:
    for x in left: 
      for y in right:
        if alphabet.index(y) > alphabet.index(x):
          return False
    
    return True 
    
  else:
    return False   




s1 = input()
s2=input()

s1=s1.upper()
s2=s2.upper()



  

if checkPat(s1):
  print("YES")
else:
  print("NO")

if checkPat(s2):
  print("YES")
else:
  print("NO")

if checkPat(s1+s2):
  print("YES")
else:
  print("NO")
