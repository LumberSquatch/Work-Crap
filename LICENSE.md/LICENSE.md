# Chris Adamick
# 1508093
#
# Programming Assignment 3

# Part 1

import csv

File = 'CF-Spring2018-Employers.csv'
InFile = open(File)
reading = csv.reader(InFile)


Rows = {}
countUp = 0
for row in reading:
    if row[0] == 'Company':
        while countUp < len(row):
            Rows[countUp] = row[countUp]
            print(str(countUp) + ' ' + Rows[countUp])
            countUp += 1



ABCrows = []
nextRow = 0
for row in reading:
    if nextRow > 3 and nextRow < 34 and row[0] != '':
        ABCrows.append(row)
    nextRow += 1

print(ABCrows)
nextRow = 0
for row in ABCrows:
    print(nextRow, ','.join(row))
    nextRow += 1
