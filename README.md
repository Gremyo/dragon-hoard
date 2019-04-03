  
![alt](./assets/logo_desc.PNG)  

# Commands

**`request`**   
Pings the targeted user and either has them respond with $accept or $deny (not case sensitive) for the amount stated, otherwise it times out.
```
!request @user amount
 
$accept, $deny 
```
---- 
**`give`**  
Transfers the amount stated to the targeted user balance, from the author's balance
```
!give @user amount 
```
---- 

**`destroy`**  
Removes the amount stated from the authors balance, permanently
```
!destroy amount
```
---- 

**`rob`**  
Allows the author to rob the targeted user for the state amount.

Targets may only be robbed once every 24 hours.

Upon successfully invoking the rob command, the targeted user is pinged and has 30 seconds to say "$run" (not case sensitive)

If they do not reply within 30 seconds, there is a 50% chance the robbery will fail. If they do reply, then there is a 50-75% chance that the robbery will fail

If the robbery fails, then the author loses half the amount stated, but not exceeding their current balance. This is transferred to the targeted user

If the robbery succeeds, then the author gains the full amount, taking it from the targeted user's balance
```
!rob @user amount
 
$run
```
---- 


# Setup  

**install discord.py**  
Dragon hoard runs on forked version of version of `discord.py` referred to as "the rewrite". 
you can install it by running the following command:    

```
python3 -m pip install -U git+https://github.com/Rapptz/discord.py@rewrite
```
  
  
**private key**    
In `private_key.py`, find and replace `token` with your discord token. 
  
```
nano private_key.py
```

``` 

private_key 

```

