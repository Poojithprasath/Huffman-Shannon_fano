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

<img width="700" height="1000" alt="WhatsApp Image 2026-05-02 at 11 53 45 AM" src="https://github.com/user-attachments/assets/fb465394-75ed-41c5-a48f-31fba9007e7a" />
<img width="700" height="1000" alt="WhatsApp Image 2026-05-02 at 11 53 45 AM (1)" src="https://github.com/user-attachments/assets/deb5f1ce-a93f-4fe4-b7bc-8b1835658a97" />
<img width="700" height="1000" alt="WhatsApp Image 2026-05-02 at 11 56 23 AM" src="https://github.com/user-attachments/assets/828fe329-a4ca-4f20-b231-dd10f2c72e6e" />



# Output

<img width="553" height="439" alt="image" src="https://github.com/user-attachments/assets/f05d26c5-eef1-4398-8da9-72b88431759c" />
 
# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
