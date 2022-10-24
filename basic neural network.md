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

