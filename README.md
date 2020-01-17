# declaration-of-independence
#Noah Ukura
#Int. Programming with Python 1/16/2020


import csv
#variables=self explanitory, num means number
total = 0
num_records = 0
num_over = 0
over = 0

print("                                 Max                Attending             Over")



with open("D:/lab2a.csv") as csvfile:
    file = csv.reader(csvfile)
    for record in file:
        num_records = num_records + 1
        total = total + int(record[2])
        if int(record[2]) > int(record[1]):
            num_over = num_over + 1
            over = int(record[2]) - int(record[1])
            print("{:31} {:20} {:14} {:10}".format(record[0], record[1], record[2], over))
     
        
    
       




print(num_records, "total rooms processed")
print(num_over, "total rooms over the maximum")
