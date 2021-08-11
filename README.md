# pwhash
A Python3 script to hash passwords (SHA512) and optionally verify the password works against the hash that was generated.

Usage:

Run `pwhash` and follow the prompt for the password you wish to hash (will not echo).

Or `pwhash` will also take the password from STDIN.

### Example 1, passwords match or skip verification
```
$ ./pwhash
Password:
$6$oEJApLSD7lRkNwo1$aCL3u.dkvhf1VQj9kl1.wASPafNPY9.pWCor03Gn/Zx3A.XDbN7n0ZB/f3gsKlZbnBaf.Hnnn.MQ04.1zmx0x.
Verify Password (Optional):
```

### Example 2, passwords do not match
```
$ ./pwhash
Password:
$6$i7HX2zxZlro.lSFx$lihoVkch.IGMR.Zm5umh0s8zj6YYXna.YYBu6S5vtHYB7/oi6LURwkPUKHQuzg902FS8mxJrp9Ru0TJh2ihRQ.
Verify Password (Optional):
Passwords did not match!
```

### Example 3, use STDIN
```
$ echo "test" | ./pwhash
$6$l9nU.NJUuJYxHmOr$O/xlOQPnVrv48BI1zkVkWXusBz5z74K0AAt0bc3cA/AHSWHP06lA/xwiiyhMX/.sQL.vcwjMemhFZTm6duj0h.
```

If you do not enter the password a second time it is OK, just press enter and the command will exit.

If you enter the password a second time and it does match, the command will exit silently.

If you enter the password a second time and it does not match, the command will tell you "Passwords did not match!"
