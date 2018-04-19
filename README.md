DNEPSA
======
A Dual  Network Exterior Point Simplex Type Algorithm for the solution of the
Minimum Network Flow Problem.

Algorithm implemented in C.
--------------------------

v1.8.1
- Change the way I_ and I+ are renewed. (in case it is th1<=th2 then I[i]=1...)

v1.8
- Make array I to contain DENSITY elements where it is -1 for I_
 and +1 for I+ and 0 is non-basic.
- So, functions calc_I, print_I etc has been changed.
- Function get_index added to give the index of an arc in FROM[] TO[] structures
- Functions find_th1, find_th2 changed in order to return the above index (it is named index_i)

v1.7.1
new:
use double instead of float for logos, s[] and t[]

v1.7
- Calculate D direction and then values t[i]=s[i]+a*D[i] where a=logos. i.e. t gives a sequence of
dual variables that are always dual feasible.
- Changed the way I_ and I+ are formes. I_ contains the non-basic arcs where sij<0 and I+ the non-basic arcs where
sij>=0.
- Better comments
- Better printings
- No need for ptint_basic_tree (Use of print_tree instead)
