# neo
### temporary sms right from your terminal

neo is a terminal script written in POSIX-compliant sh that allows you to get a temporary phone number and receive messages.
it uses [upmasked](https://upmasked.com), a temp sms service in order to recieve the messages.
this is a very useful tool for people who don't have phone numbers, and schizos.

### dependencies
- curl
- jq
- fzf

### installation
```
$ git clone https://github.com/lainplus/neo
$ cd neo
$ chmod +x neo
$ sudo mv neo /usr/bin
$ cd ..
$ rm -rf neo/
```

### usage

initialize a new phone number

```
$ neo init
```

view the 5 newest messages. by default neo shows the 3 newest messages.

```
$ neo -c 5
```

if you find it annoying to rerun neo every few seconds or so, use watch with a delay of 5 seconds.
upmasked only updates messages every 5 seconds anyway.

```
$ watch -n 5 "neo"
```

