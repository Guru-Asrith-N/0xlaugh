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
