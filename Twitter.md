# Authentification Twitter

- Open the file with wireshark
- We only see one packet ```HTTP Protocol```
- Let's open the packet to see what's inside of it :
  - Let's look at the last line ```Hypertext Transfer Protocol```
    ```
    Hypertext Transfer Protocol
        GET /statuses/replies.xml HTTP/1.1\r\n
            [Expert Info (Chat/Sequence): GET /statuses/replies.xml HTTP/1.1\r\n]
            Request Method: GET
            Request URI: /statuses/replies.xml
            Request Version: HTTP/1.1
        User-Agent: CFNetwork/330\r\n
        Cookie: _twitter_sess=BAh7CDoJdXNlcjA6B2lkIiVmZGQ2ODc5MTMwMWFhOTFiMWExZDViZmQwMGEz%250AOWNkMyIKZmxhc2hJQzonQWN0aW9uQ29udHJvbGxlcjo6Rmxhc2g6OkZsYXNo%250ASGFzaHsABjoKQHVzZWR7AA%253D%253D--ea12e7bc090d05202cd7e3f972c2b4414a97f657\r\n
            Cookie pair: _twitter_sess=BAh7CDoJdXNlcjA6B2lkIiVmZGQ2ODc5MTMwMWFhOTFiMWExZDViZmQwMGEz%250AOWNkMyIKZmxhc2hJQzonQWN0aW9uQ29udHJvbGxlcjo6Rmxhc2g6OkZsYXNo%250ASGFzaHsABjoKQHVzZWR7AA%253D%253D--ea12e7bc090d05202cd7e3f972c2b4414a97f657
        Accept: */*\r\n
        Accept-Language: en-us\r\n
        Accept-Encoding: gzip, deflate\r\n
        Authorization: Basic dXNlcnRlc3Q6cGFzc3dvcmQ=\r\n
            Credentials: usertest:********
        Connection: keep-alive\r\n
        Host: twitter.com\r\n
        \r\n
        [Full request URI: http://twitter.com/statuses/replies.xml]
        [HTTP request 1/1]
    ```
    - Let's focus on the ```Authorization``` part:
      - On the first line we see some weird Base64 encoded text : ```dXNlcnRlc3Q6cGFzc3dvcmQ=```
      - On the next line, we see ```Credentials: usertest:********``` the value after the ```:``` is intentionally hidden, this is the username/password pair 
      - We found the flag !!!
      - We can also convert this ```dXNlcnRlc3Q6cGFzc3dvcmQ=``` to readable text, we'll get the same thing 