# -*- coding: utf-8 -*-
"""
Created on Thu Jan 28 21:57:31 2021

@author: damla.yildiz
"""


#Pizza MIS 
Newyork=['Mozarella','Pepperoni','Basil','Green Pepper']

Veggie=['Mozarella', 'Mushroom', 'Green Pepper', 'Onion']

Margarita=['Spicy Tomato Sauce', 'Mozarella']

BBQ=['Mozarella', 'BBQ Sauce','Grilled Chicken', 'Onion' ]

Extra=['Olive','Salami','Sausage','Corn']
extselect=[]
print("                                     Welcome to Pizza Little Italy")
print("                                                 Menu")
print("1-Newyork: 12$" )
print(Newyork[0], Newyork[1], Newyork[2], Newyork[3],sep=', ')
print("2-Veggie: 10$")
print(Veggie[0], Veggie[1], Veggie[2], Veggie[3],sep=', ')
print("3-Margarita: 8$")
print(Margarita[0], Margarita[1],sep=', ')
print("4-BBQ: 15$")
print(BBQ[0], BBQ[1], BBQ[2], BBQ[3],sep=', ')
print("+Extra Ingridients: ")
print(Extra[0], '2$')
print(Extra[1], '3$')
print(Extra[2], '4$')
print(Extra[3], '1$')
def price(list) :
    
    if list==Newyork:
        
        if len(Newyork)== 4:
            return  12
        elif len(Newyork)!=4:
            ingr_count_ext= list.count('Olive')*2 + list.count('Salami')*3 + list.count('Sausage')*4 + list.count('Corn')*1
            final_price= 12 + ingr_count_ext
            return final_price
    if list==Veggie:
        if len(Veggie)== 4:
            return  10
        elif len(Veggie)!=4:
            ingr_count_ext= list.count('Olive')*2 + list.count('Salami')*3 + list.count('Sausage')*4 + list.count('Corn')*1
            final_price= 10 + ingr_count_ext
            return final_price
    if list==Margarita:
        
         if len(Margarita)== 4:
            return  8
         elif len(Margarita)!=4:
            ingr_count_ext= list.count('Olive')*2 + list.count('Salami')*3 + list.count('Sausage')*4 + list.count('Corn')*1
            final_price= 8 + ingr_count_ext
            return final_price
    if list==BBQ:
        
         if len(BBQ)== 4:
            return  15
         elif len(BBQ)!=4:
            ingr_count_ext= list.count('Olive')*2 + list.count('Salami')*3 + list.count('Sausage')*4 + list.count('Corn')*1
            final_price= 15 + ingr_count_ext
            return final_price
         
price  

selection=input("Which one do you prefer?: ")


extra= input('Would you like to add extra ingridients? Yes or No: ')



if extra== 'Yes':
    if selection=='Newyork':
          extselect=input("Enter the extra ingridient you want to add your pizza: ")
          try: 
              extselect_index=Extra.index(extselect)
              Newyork.insert(0,extselect)
              print("Here is your pizza ingridients: ", Newyork)
          except ValueError:
                  print("That item was not found in the Extra list")
          remove= input("Would you like to remove some of the ingridient? Yes or No: ")
          if remove== 'Yes': 
                rmvselect=input("Enter the ingridient you want to remove from your pizza: ")
                try: 
                        Newyork.remove(rmvselect)
                        print("Here is your selection: ")
                        print(Newyork)
                        print ("Here is your pizza price: ", price(Newyork))
                except ValueError:
                    print("That item was not found in the list ")
                    print ("Here is your pizza price: ", price(Newyork))
          if remove=='No':
                print("Here is your pizza price: " , price(Newyork))
    if selection=='Veggie':
          extselect=input("Enter the extra ingridient you want to add your pizza: ")
          try: 
              extselect_index=Extra.index(extselect)
              Veggie.insert(0,extselect)
              print("Here is your pizza ingridients: ", Veggie)
          except ValueError:
                  print("That item was not found in the Extra list")
          remove= input("Would you like to remove some of the ingridient? Yes or No: ")
          if remove== 'Yes': 
                rmvselect=input("Enter the ingridient you want to remove from your pizza: ")
                try: 
                        Veggie.remove(rmvselect)
                        print("Here is your selection: ")
                        print(Veggie)
                        print ("Here is your pizza price: ", price(Veggie))
                except ValueError:
                    print("That item was not found in the list ")
                    print ("Here is your pizza price: ", price(Veggie))
          if remove=='No':
                print("Here is your pizza price: " , price(Veggie))
    if selection=='BBQ':
          extselect=input("Enter the extra ingridient you want to add your pizza: ")
          try: 
              extselect_index=Extra.index(extselect)
              BBQ.insert(0,extselect)
              print("Here is your pizza ingridients: ", BBQ)
          except ValueError:
                  print("That item was not found in the Extra list")
          remove= input("Would you like to remove some of the ingridient? Yes or No: ")
          if remove== 'Yes': 
                rmvselect=input("Enter the ingridient you want to remove from your pizza: ")
                try: 
                        BBQ.remove(rmvselect)
                        print("Here is your selection: ")
                        print(BBQ)
                        print ("Here is your pizza price: ", price(BBQ))
                except ValueError:
                    print("That item was not found in the list ")
                    print ("Here is your pizza price: ", price(BBQ))
          if remove=='No':
                print("Here is your pizza price: " , price(BBQ))
    if selection=='Margarita':
          extselect=input("Enter the extra ingridient you want to add your pizza: ")
          try: 
              extselect_index=Extra.index(extselect)
              Margarita.insert(0,extselect)
              print("Here is your pizza ingridients: ", Margarita)
          except ValueError:
                  print("That item was not found in the Extra list")
          remove= input("Would you like to remove some of the ingridient? Yes or No: ")
          if remove== 'Yes': 
                rmvselect=input("Enter the ingridient you want to remove from your pizza: ")
                try: 
                        Margarita.remove(rmvselect)
                        print("Here is your selection: ")
                        print(Margarita)
                        print ("Here is your pizza price: ", price(Margarita))
                except ValueError:
                    print("That item was not found in the list ")
                    print ("Here is your pizza price: ", price(Margarita))
          if remove=='No':
                print("Here is your pizza price: " , price(Margarita))
    

                
                
                
                
elif extra=='No':
    
    remove= input("Would you like to remove some of the ingridient? Yes or No: ")
    if remove== 'Yes':
        rmvselect=input("Enter the ingridient you want to remove from your pizza: ")
        try: 
            if selection== 'Newyork':
                Newyork.remove(rmvselect)
                print("Here is your selection: ")
                print("Here is your pizza price: " , price(Newyork))
            if selection=='Veggie':
                Veggie.remove(rmvselect)
                print("Here is your selection: ")
                print("Here is your pizza price: " , price(Veggie))
            if selection== 'Margarita':
                Margarita.remove(rmvselect)
                print("Here is your selection: ")
                print("Here is your pizza price: " , price(Margarita))
            if selection== 'BBQ':
                BBQ.remove(rmvselect)
                print("Here is your selection: ")
                print("Here is your pizza price: " , price(BBQ))
            
        except ValueError:
            print("That item was not found in the list ")
    if remove=='No':
          if selection== 'Newyork':
                print("Here is your pizza price: " , price(Newyork))
          if selection=='Veggie':
                print("Here is your pizza price: " , price(Veggie))
          if selection== 'Margarita':
                print("Here is your pizza price: " , price(Margarita))
          if selection== 'BBQ':
                print("Here is your pizza price: " , price(BBQ)) 
