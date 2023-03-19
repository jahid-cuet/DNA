import pandas as pd
file = pd.read_csv('C:\\Users\DELL\Desktop\country_2.txt',delimiter=' ')
file.head()
input_value=input()
result=file[file.Patient_Name == input_value]
if(len(result)):
    dna=result['dna_data'].to_string(index=False)
    print(dna)
else:
    print('Invalid')
file.loc[0]['dna_data']
Data = list(file['dna_data'])
print(Data)
dna2 = dna[ : :-1]
print(len(dna2))
import random, sys, time
PAUSE = 0.15
ROWS = [
    
    '        ##', # Index 0 has no {}.
    '      #{}-{}#',
    '     #{}---{}#',
    '    #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '   #{}-----{}#',
    '    #{}---{}#',
    '      #{}-{}#',
    '        ##',     #9
    '     #{}-{}#',
    '    #{}---{}#',
    '    #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '   #{}-----{}#',
    '     #{}---{}#',
    '       #{}-{}#',
    '         ##',   #18
    '       #{}-{}#',
    '     #{}---{}#',
    '    #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '   #{}-----{}#',
    '   #{}---{}#',
    '     #{}-{}#',
    '        ##',    #27
    '     #{}-{}#',
    '    #{}---{}#',
    '   #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '    #{}-----{}#',
    '     #{}---{}#',
    '      #{}-{}#',
    '        ##',   #36
    '      #{}-{}#',
    '     #{}---{}#',
    '    #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '   #{}-----{}#',
    '     #{}---{}#',
    '      #{}-{}#',
    '        ##',   #45
    '     #{}-{}#',
    '    #{}---{}#',
    '   #{}-----{}#',
    '   #{}------{}#',
    '   #{}------{}#',
    '   #{}-----{}#',
    '    #{}---{}#',
    '     #{}-{}#',
    '        ##',

    ]

print('DNA Animation')
print('Press Ctrl-C to quit.')
rowIndex = 0


    
for i,j in zip(dna,dna2):
    rowIndex = rowIndex + 1
    if rowIndex == len(ROWS):
        break
         # Row indexes 0 and 9 don't have nucleotides
    if rowIndex == 0 or rowIndex == 9 or rowIndex==18 or rowIndex==27 or rowIndex==36 or rowIndex==45:
        continue
    print(ROWS[rowIndex].format(i,j))