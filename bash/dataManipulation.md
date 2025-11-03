
## cut

The "cut" command allows you to extract data from an input. 

In pwn.college there is useful example. 

https://pwn.college/linux-luminarium/data/

The flag script (/challenge/run) outputs random characters next to the flag in two columns. 

We use "cut" for removing this first column with random characters. 

`cut -d " " -f 2` => leaves only the second column, the one with the flag. 

Now we have to pipe it with tr. 

`tr -d "\n"` => removing the line breaker. 

The complete command: 

`/challenge/run |cut -d " " -f 2 | tr -d "\n"`


