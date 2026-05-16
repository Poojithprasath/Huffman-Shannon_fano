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

<img width="700" height="1000" alt="WhatsApp Image 2026-05-16 at 11 07 57 AM" src="https://github.com/user-attachments/assets/9fa358ea-ea8e-4afe-9155-33ec76bf2b31" />
<img width="700" height="1000" alt="WhatsApp Image 2026-05-16 at 11 09 42 AM" src="https://github.com/user-attachments/assets/029f4497-1f09-429c-855e-bedc3efb3e7e" />
<img width="700" height="1000" alt="WhatsApp Image 2026-05-16 at 11 09 13 AM" src="https://github.com/user-attachments/assets/426794cf-f589-4b07-9e71-a0996bd618dd" />


# Output

<img width="553" height="439" alt="image" src="https://github.com/user-attachments/assets/f05d26c5-eef1-4398-8da9-72b88431759c" />
 
# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
