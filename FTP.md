## FTP Auth

- Opened the file with wireshark
- Applied a filter to see only the FTP sent data
  - Prompted ``` ftp-data ``` on wireshark
- Searched for a FTP request with the words ``` USER ``` or ``` PASSWORD ```
  - Found the lines bellow
    - ```Request command: USER```
    - ```Request arg: cdts3500```
  - These response was given after the request were sent 
    - ```Response code: User name okay, need password (331)```
    - ```Response arg: Enter password.```
  - Then, the password was sent as a request
    - ```Request command: PASS```
    - ```Request arg: ********```

    
