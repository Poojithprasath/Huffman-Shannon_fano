# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Software Required:
Google Collab
# Program:
```sci
# Huffman and Shannon-Fano Coding
import math

n = int(input("Enter number of samples: "))

p = [float(input(f"Probability {i+1}: ")) for i in range(n)]
l = [float(input(f"Length {i+1}: ")) for i in range(n)]

L = sum(p[i]*l[i] for i in range(n))
H = round(sum(p[i]*math.log2(1/p[i]) for i in range(n)), 3)

eff = round(H/L, 3)
red = round(1-eff, 3)
var = round(sum(p[i]*(l[i]-L)**2 for i in range(n)), 3)

print("Average Codeword Length:", L)
print("Entropy:", H)
print("Efficiency:", eff)
print("Redundancy:", red)
print("Variance:", var)
```
# Calculation:

<img width="407" height="400" alt="WhatsApp Image 2026-05-02 at 11 02 55 AM" src="https://github.com/user-attachments/assets/e2c3e5b7-8a86-455f-8f15-ba7a8741a09f" />
<img width="450" height="450" alt="WhatsApp Image 2026-05-02 at 11 03 05 AM" src="https://github.com/user-attachments/assets/63ba1d9c-ada1-46c4-8339-43c1af99cac9" />



# Output

<img width="553" height="439" alt="image" src="https://github.com/user-attachments/assets/f05d26c5-eef1-4398-8da9-72b88431759c" />
 
# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
