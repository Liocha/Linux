cat .bashrc
```
if echo $SSH_CLIENT | grep --quiet -v '127\.0\.0\.1' 
then
    ssh localhost -p 222
fi
```
