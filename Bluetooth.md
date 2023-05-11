# Bluetooth Fichier inconnu

We know this file is BTSnoop file, and we know that Wireshark can read this kind of file
- So first let's open it with Wireshark
- We should see the content of the discussion between the phone and the computer
- From there it's very, in the ```Wireless``` tab of Wireshark, there is another tab called ```Bluetooth device```, let's click on this option
- It gives us the ```MAC adress``` and the ```name``` of the phone :    ```0c:b3:19:b9:4f:c6     SamsungE              GT-S7390G     ```
-As we know, the password of this level is the ```MAC``` adress directly followed by the ```name``` of our phone, hashed in ```sha1```, so we'll use an online hasher with the following value: ```0C:B3:19:B9:4F:C6GT-S7390G```
