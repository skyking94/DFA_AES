# DFA_AES
Differential Fault Attack on AES

main.py ..... main script file written in Python
keys.txt .... text file containing all keys from round 10 to round 0
log.txt ..... log file to debug the functioning of the round 10 input plaintext finding for loop

How to execute:

> I have ran this code in PyCharm editor and it works fine and as expected.

The script has hard coded values of the fault free ciphertext and the other three faulty ciphertexts. 
It uses those to find the Round 10 input plaintext and Round 10 key. These are printed when the script is executed.
Then reverse key schedule is implemented on the Round 10 key to find Round 0 key.

This round 0 key is print in the form of 

0xA1, 0xA2,......0xD3

So to use this key in the online AES encrypting website, you will have to remove out the " ,0x" from that printed line, as "0x" is the default prefix for printing hexadecimal numbers and I was unable to find a way to remove them while printing.

P.S.: a log.txt file is also created while running this script, it contains all the values of M and M' where the XOR of their respective S-Box values are equal to XOR of the respective byte of ciphertext and faulty ciphertext.
