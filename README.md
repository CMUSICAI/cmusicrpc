# CmusicAI RPC

Crazy simple CmusicAI RPC library, designed to work with all versions of CmusicAI.

*"I have seen many libraries, this one... is pretty average" - Joe*

INSTALL:

```
pip install cmusicairpc
```

## Setting Up cmusicaid (Linux)

go to your `.cmusicai` folder, add a `cmusicai.conf` file if there is not one already, in that file add:

```
rpcuser=username
rpcpassword=password
```

**Make sure you use a secure username and password!**

Then run `./cmusicaid` in the directory that it is located!

Examples:

```python
from cmusicairpc import CmusicAI

cmusicai = CmusicAI('username', 'password')
cmusicai.getinfo()
cmusicai.listreceivedbyaddress(0, True)
```

Any other rpc method:

```python
cmusicai.<METHOD>(<param1>, <param2>, ...)
```

**Note**: If the username and password are incorrect, then a empty string will be returned. 

Please report any bugs by filling out an issue!

## Use it with other cryptos too!!

Just set the port when accessing:

```python
btc = CmusicAI('username', 'password', port=8332)
```

And if you want to use a different host:

```python
btc = CmusicAI('username', 'password', host='host.com', port=8333)
```
