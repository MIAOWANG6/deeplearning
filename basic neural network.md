# Neural network Representation

<img src="https://user-images.githubusercontent.com/52966164/197487515-68137500-ba0f-4764-bef3-52c91aa3ef10.png" width=40% />

<img src="https://user-images.githubusercontent.com/52966164/197488380-c718247a-1043-45e8-8159-b7902cf54693.png" width=80% />

# Vectorization for single sample
### $a^{[1]}=\sigma(w^{[1]T}\cdot x+b^{[1]})$

### $(N_{neu},1)=(N_{fea},N_{neu})^T\cdot (N_{fea},1)+(N_{neu},1)$

### $a^{[2]}=\sigma(w^{[2]T}\cdot a^{[1]}+b^{[2]})$

### $(1,1)=(N_{neu},1)^T\cdot (N_{neu},1)+(1,1)$

# Vectorization for multiple samples

<img src="https://user-images.githubusercontent.com/52966164/197491279-e9af098a-7b06-42e2-84e4-d08a1d7dc183.png" width=30% />

<img src="https://user-images.githubusercontent.com/52966164/197491585-47ff4072-6f85-43d8-bb22-f8244b88426d.png" width=55% />

### $A^{[1]}=\sigma(W^{[1]T}\cdot X+b^{[1]})$

### $(N_{neu},N_{sub})=(N_{fea},N_{neu})^T\cdot (N_{fea},N_{sub})+(N_{neu},N_{sub})$

### $A^{[2]}=\sigma(W^{[2]T}\cdot A^{[1]}+b^{[2]})$

### $(1,N_{sub})=(N_{neu},1)^T\cdot (N_{neu},N_{sub})+(1,N_{sub})$

# Activation function

## $a=tanh(z)=\frac{e^z-e^{-z}}{e^z+e^{-z}}$ （双曲正切函数）

<img src="https://user-images.githubusercontent.com/52966164/197495284-195de2a4-190c-44cc-b55a-47452d2fc297.png" width=40% />

### because it is around 0, have effect like centerization.

### tanh is always better than sigmoid, except for output layer, whose 0/1 results make it suitable for signoid

### However, a disadvantage exists for both tanh and sigmoid, the gradient ( $\frac{dL}{dz}$ ) become very small when z is large or small enough, the learning will be slow.

## ReLU (线性修正函数) $a=max(0,z)$
<img src="https://user-images.githubusercontent.com/52966164/197711655-c6ab2435-7e79-49a9-979f-cc5aa07cd34a.png" width=40% />

### It is often used now when you can't figure out what is better. Fast learning.

### Its only disadvantage is gra=0 when z is negative, which promotes "leaky ReLU" to be appeared.

## Non-linear activation function

### Why we need an non-linear activation function to remap linear input $z^{[1]}=w^Tx+b$ and then $z^{[2]}$ to nonlinear space.

### If not, the output will just be the linear combination of its input. Like a k layers network with linear activation and a sigmoid output layer, is just as same as simple logistic regression

### Importantly, ReLU is nonlinear activation in the level of different samples

![image](https://user-images.githubusercontent.com/52966164/197718148-b1ecd201-da73-4a73-b2ad-1ededfb91959.png)

# Gradient Descend in NN

## derivatives of activation function

### $d(a=\sigma(z))=a\cdot (1-a)$

### $d(a=tanh(z))=1-a^2$

### $d(a=ReLU(z))=\lgroup{a}{b}$


