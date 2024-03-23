# Ex.No: 6   Logic Programming – Factorial of number   
### DATE::23/03/2024                                                                              
### REGISTER NUMBER : 212221060144
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
3.  a )	If only one disk  => Move disk from X to Y.
4.  b)	If Number of disk greater than 0 then
5.        i)	Move  N-1 disks from X to Z.
6.        ii)	Move  Nth disk from X to Y
7.        iii)	Move  N-1 disks from Y to X.
8. Run the program  to find answer of  query.

### Program:
```
% Define the predicate hanoi/3 to solve the Towers of Hanoi problem
hanoi(1, X, Y) :-
    write('Move disk from '), write(X), write(' to '), write(Y), nl.

hanoi(N, X, Y) :-
    N > 1,
    M is N - 1,
    hanoi(M, X, Z),
    hanoi(1, X, Y),
    hanoi(M, Z, Y).
```
### Output:
![image](https://github.com/Chandru0021/AI_Lab_2023-24/assets/131637082/7a49caee-635b-4ae8-94f5-0a1ea25b4df3)
### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.
