## Descripción:
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

`ssh -p 52236 ctf-player@atlas.picoctf.net`Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

Hints:
- Have you ever played hot or cold? Binary search is a bit like that.
- You have a very limited number of guesses. Try larger jumps between numbers!
- The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solución:
```
artacas-picoctf@webshell:~$ ssh -p 52236 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:52236 ([18.217.83.136]:52236)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:52236' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 200
Higher! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 500
Higher! Try again.
Enter your guess: 600
Lower! Try again.
Enter your guess: 550
Lower! Try again.
Enter your guess: 520
Lower! Try again.
Enter your guess: 510
Higher! Try again.
Enter your guess: 515
Higher! Try again.
Enter your guess: 518
Lower! Try again.
Enter your guess: 517
Congratulations! You guessed the correct number: 517
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.
artacas-picoctf@webshell:~$ 
```

