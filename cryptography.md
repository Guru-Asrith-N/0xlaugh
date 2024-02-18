# Cryptography

### RSA GCD

opened the challenge  
understood that it is a RSA cipher so tried to find the corresponding variables   
found the eqn c=pow(m,eq1,n)   
so eq1 will be the encryption key  
and eq1 is given as 'eq1 = next_prime(out1)' hence the prime after out1 is eq1  
and out 1 is 'out1=pow((p+5*q),power1,n)'  
where power1 is given and p and q are variable used in RSA algorithm   
power2 is also given and you can get ou2 also from 'out2=pow((2*p-3*q),power2,n)'   
on solving both ou1 and out2 you can get p and q   
using p and q you can find phi through which you can get max value of encryption key  '1 < e < phi'   
which is eq1 which is given  
we can find decryption key which is "multiplicative inverse of e mod phi"   
we can use 'm=c^e mod n' to find m   

### L4ugh

opened the challenge  
read the utils file  
from evilRSA we get a prime from 6 to 9 th position of seed  
from RSAgen we get the parameters for RSA like p,q,etc   
from encrypt we get AES encryption of message and vice versa for decryption  
in flag function if required data is entered we get flag  
read challenge page   
key is a random 16 bit number 
x is random number from 2^10 to 2^20   
d_evil = d >> (int(seed[6:9])//2) you get the second part of the key  
d_good = d %  pow(2,int(seed[6:9])//2) you get the first part of the key  
from test function we get the parameters of RSA if we enter option 1   
from option 2 we get random from d_good    
from option 3 if we select option 2 of z and if we decrypt token then we get the flag   
