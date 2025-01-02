# brute-force
A Python project that uses brute force to crack a simple password by systematically generating and testing all possible character combinations. It highlights the inefficiency of brute force and emphasizes the importance of strong passwords.

import itertools
import string
import time

print("HELLO YADAV JI I AM PASSWORD FINDER CODED BY BABA")
chars = string.printable

password = "@65"

max_length = 10

start_time = time.time()

for length in range(1,max_length + 1):
    for combination in itertools.product(chars, repeat=length):
        candidate ="".join(combination)
        print("Typing password:", candidate)
        if candidate == password:
            end_time = time.time()
            print("HEY DARLING I FOUND YOUR PASSWORD:",candidate)
            time_taken = end_time - start_time
            print("Time taken:",time_taken,"seconds")
            raise SystemExit
