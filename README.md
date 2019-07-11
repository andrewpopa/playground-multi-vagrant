# playground-multi-vagrant
Example of multiple Vagrant machines in one file

Environment description
```
web1
web2
mysql
```

Create environment 

```bash
vagrant up
```
Login to machines

```
vagrant ssh web1
```

Destory machines

```
vagrant destroy -f
```