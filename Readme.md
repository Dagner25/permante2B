Permanete2B
Lo primero que se hizo fue modicar un codigo a formato pyton, dichos codigos son los que se pueden apreciar en la parte de abajo, estan divididos en dos, los cuales son: 
-Insertion_sort
-Bubblesort

import random
import time




def INSERTION_SORT(A):
    for j in range(1,len(A)):
        key = A[j]
        i = j - 1
        while i >= 0 and key < A[i]:
            A[i+1] = A[i]
            i = i - 1
        A[i+1] = key
    return A 

def BUBBLESORT(L):
    n = len(L)
    for i in range(0, n):
        for j in range(n-1, i, -1):
            if L[j] < L[j-1]:
                key = L[j]
                L[j] = L[j-1]
                L[j-1] = key
    return L

Despues de haber cambiado el codigo a formato python lo que hizimos fue dar un valor a "n" para que despues creemos otra bandeja de codigo.Para hallar la cantidad de tiempo que demorara en hacer dicha accion.
n = 10000
 
lista = list(range(n))

random.shuffle(lista)

tiempo_inicial = time.time()
ordenada = INSERTION_SORT(lista)
tiempo_final = time.time()

print(tiempo_final - tiempo_inicial)

random.shuffle(lista)

tiempo_inicial = time.time()
ordenada = BUBBLESORT(lista)
tiempo_final = time.time()

print(tiempo_final - tiempo_inicial)

Al finalizar en una grafica pusimos cuanto fue que demoro, con distintos valores a "n"