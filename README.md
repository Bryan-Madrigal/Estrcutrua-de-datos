# Bryan Raul Perez Madrigal 3J LSC - Manejo de memoria 
maxf= 3
maxc= 5
a= [[0.0]*maxc for_in range(maxf)]
 
 #leer array
 for f in range(maxf):
 for c in range(maxc):
 a[f][c]= float(input())

#escribir el array 
 for f in range(maxf):
 for c in range(maxc):
 print (a([f][c]), end="")
print()
