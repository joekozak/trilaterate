# Trilaterate
Python trilateration module for arbitrary dimensional space

Instructions:

takes [distance,coordinate] pairs of the form: 
[[d1,[x11,x12,x13,...,x1n]],[d2,[x21,x22,...,x2n],...]

requires n+1 points minimum, uses first n+1 points given
returns false if less than n+1 points provided

returns n dimensional coordinates of unknown point as array [y1,y2,...,yn]

returns false if data is invalid (incorrectly formatted or unsolvable)
returns false if first n+1 points are not unique or non-colinear

Example:

import trilaterate

pointdata = [[1,[1,0,0,0]],
            [1,[0,1,0,0]],
            [1,[0,0,1,0]],
            [1,[0,0,0,1]],
            [2,[1,1,1,1]]]
            
p = trilaterate.trilaterate(pointdata)

print(p)

[0, 0, 0, 0]
