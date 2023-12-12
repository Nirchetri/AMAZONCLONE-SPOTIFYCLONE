#Practical 1A
'''Q1.A) Addition Of Two Complex Numbers'''
a = 4 + 2j
b = 3 - 5j
print("Addition Of Two Complex Numbers Is", a+b)


#Practical 1B
'''Q1.B) Conjugate Of A Complex Number'''
a = 4 + 2j
a.conjugate()


#PRACTICAL 1C
'''Q1.C) Plotting A Set Of Complex Numbers'''
import matplotlib.pyplot as plt
x = 2 + 2j
a = [-2+4j, -1+2j, 0+2j, 1+2j, 2+2j, -1+4j, 0+4j, 1+4j]
X = [x.real for x in a]
Y = [x.imag for x in a]
plt.scatter(X,Y, color='red')
plt.show()



#PRACTICAL 2 (Rotation For 90 Degree)
'''Creating A New Plot By Rotating The Given Number By A Degree 90, 180, 270
Degrees And Also By Scaling By A Number a = 1/2, a = 1/3, a = 2 etc '''
import matplotlib.pyplot as plt
x = 2 + 4j
z = 1j
plt.scatter(x.real,x.imag,color='red')
c = x * z
plt.scatter(c.real, c.imag)
plt.show()

#PRACTICAL 2 (Rotation For 180 Degree)
import matplotlib.pyplot as plt
x = 2 +4j
plt.scatter(x.real, x.imag, color='red')
plt.scatter(-1 * x.real, -1 *x.imag,color='blue')
plt.show()

#PRACTICAL 2 (Rotation For 270 Degree)
import matplotlib.pyplot as plt
x = 2 + 4j
z = -1j
plt.scatter(x.real,x.imag,color='red')
c = x * z
plt.scatter(c.real, c.imag)
plt.show()



#PRACTICAL 3
'''WAP To Do The Following
   a. Enter A Vector U As A n-list
   b. Enter Another Vector v as a n-list
   c. Find The Vector au+bv For DIfferent Values Of a And b
   d. Find The Dot Product Of u And v'''
import numpy as np

u = np.array([3, 4, 5])
v = np.array([1, 2, 7])

print("vector u", u)
print("vector v", v)

print("Enter The Value Of a and b")
a = int(input())  # Convert user input to a floating-point number
b = int(input())  # Convert user input to a floating-point number

# Perform vector operations
d = a * u + b * v
p = np.dot(u, v)

print("vector au + bv:", d)
print("dot product of u and v:", p)


#Program 4A
"""Q1.A Enter two distinct faces as vectors u and v."""
from PIL import Image
import numpy as np

# File paths to your images
file1= r'/content/boy.jpg'
file2 = r'/content/images.jpeg'

# Open the images

a= Image.open(file1)
b = Image.open(file2)

# Display the images
a.show()
b.show()

# Convert the images to manrays
numpydata1 = np.array(a)
numpydata2 = np.array(b)

# Get the shapes of the NumPy arrays
i1 = numpydata1.shape
i2 = numpydata2.shape
print(i1)
# Create new images from the shape arrays
a1 = Image.fromarray(np.zeros(i1, dtype=np. uint8))
a1.show()
b1 = Image.fromarray(np.zeros(12, dtype=np. uint8))
b1.show()


#Program 4B
""" Find a new face as a linear combination of
u and v i.e au+bv for a and b in R"""
import numpy as np
from PIL import Image
from IPython.display import display

file1 = '/content/boy.jpg'
file2 = '/content/images.jpeg'
a = Image.open(file1)
b = Image.open(file2)
# Resize an image array using PIL
def imresize(im, sz):
    pil_im = Image.fromarray(im)
    return np.array(pil_im.resize(sz))

i1 = np.array(a)
i2 = np.array(b)
# Resize image 1
r1 = imresize(i1, (200, 200))
# Resize image 2
r2 = imresize(i2, (200, 200))
x = 1
y = 0
# Perform a linear combination
linear_comb = x * r1 + y * r2

# Convert the resulting array back to an image
lincomb_img = Image.fromarray(np.uint8(linear_comb))

# Show the resulting image
print(lincomb_img)
lincomb_img.show()
display(lincomb_img)


#Program 4C
""" Find the average face of original faces """
from PIL import Image
import numpy as np
from IPython.display import display

file1 = '/content/boy.jpg'
file2 = '/content/images.jpeg'

a = Image.open(file2)
b = Image.open(file1)

a.show()
b.show()

i1 = np.array(a)
i2 = np.array(b)

print(11)
print(12)

def imageresize(im, sz):
    pil_im = Image.fromarray(np.uint8(im))
    return pil_im.resize(sz)

r1 = np.array(imageresize(i1, (300, 300)))
r2 = np.array(imageresize(i2, (300, 300)))
x = 2
y = 9
c = x * r1 + y * r2
c1 = Image.fromarray(np.uint8(c))

display(c1)


#PRACTICAL 5
'''Q5.A) Enter A r By c Matrix M(r And c Being Positive Integers)
   B) Display M In Matrix Format
   C) Display The Rows And Columns Of The Matrix M Printing Rows
   D) Find The Scalar Multiplication Of M For A Given Scalar
   E) Find The Transpose Of The Matrix M'''
import numpy as np
M = np.array([[1,1,2],[2,6,7],[3,6,7]])
print("\nM = ",M)
y1 = M[0:1]
print("\ny1 = ",y1)
y2 = M[0:2]
print("y2 = ",y2)
y3 = M[0:3]
print("y3 = ",y3)

x1 = M[:,0:1]
print("\nx1 = ",x1)
x2 = M[:,0:2]
print("x2 = ",x2)
x3 = M[:,0:3]
print("x3 = ",x3)

a = 5
scalarresult = a * M
print("\nScalar Result =", scalarresult)

T = np.array([[0,0,0],
             [0,0,0],
             [0,0,0]
            ])
for i in range(len(M)):
  for j in range(len(M[0])):
    T[j][i] = M[i][j]
print("\nTranspose =",T)


#PRACTICAL 6A
'''Q6.A) Find The Vector-Matrix Multiplication Of A r By c Matrix M
   With An c-vector u'''
import numpy as np
a = np.array([0,4,6])
b = np.array([[1, 1],[4, 9], [-1,-10]])
print(np.dot(a,b))

#PRACTICAL 6B
'''Q6.B) Find The Matrix-Matrix Product Of M With A c By p Matrix N'''
X = [[3,3,2],
    [4,1,5],
    [7,2,7]]

Y = [[5,3,1,2],
    [1,7,3,0],
    [2,5,2,1]]

MUL = [[0,0,0,0],
    [0,0,0,0],
    [0,0,0,0]]

print("MULTIPLICATION OF TWO MATRIX IS: ")
for i in range (len(X)):
  for j in range (len(Y[0])):
    for k in range (len(Y)):
      MUL[i][j] += X[i][k] * Y[k][j]

for r in MUL:
  print(r)


#PRACTICAL 7
'''Q7) WAP To Enter A Matrix And Check If It Is Invertible. If
   The Inverse Exists, Find The Inverse'''
import numpy as np
M = np.array([[1,2,1],[2,1,0],[3,0,2]])
print("The Matrix M Is: ", M)
a = np.linalg.det(M)
print("Deteminant Of Matrix M Is ", a)
if a<=0:
  Minv = np.linalg.inv(M)
  print("The Inverse Of Matrix M Is", Minv)
else:
  print("Matrix Is Not Invertible")
