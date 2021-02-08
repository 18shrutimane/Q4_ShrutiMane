# Q4_ShrutiMane
import math  
def dCount(n): 
    LM = [1] * (n + 1); 
      
    p = 2; 
    while((p * p) < n): 
        if (LM[p] == 1): 
            for i in range((p * 2), n, p): 
                LM[i] = 0; 
        p += 1; 
 
    total = 1; 
    for i in range(2, n + 1): 
        if (LM[p] == 1): 
            count = 0; 
            if (n % i == 0): 
                while (n % i == 0): 
                    n = int(n / i); 
                    count += 1; 
                total *= (count + 1); 
                  
    return total;

def dSum(n) : 
    if(n == 1): 
       return 1
  
    result = 0

    for i in range(2,(int)(math.sqrt(n))+1) : 
  
        if (n % i == 0) : 
            if (i == (n/i)) : 
                result = result + i 
            else : 
                result = result + (i + n//i) 
    return (result + n + 1) 
  

n = 42; 
print(dCount(n)); 
print(dSum(n))
n= 147
print(dCount(n)); 
print(dSum(n))
