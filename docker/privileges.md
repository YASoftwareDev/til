Let’s now create a dummy user and group

```
useradd --user-group --system --create-home --shell /bin/bash --no-log-init app
```

now list users:
```
cat /etc/passwd
```

and switch to it:
```
su - app
```
