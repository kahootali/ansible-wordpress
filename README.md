# ansible-wordpress
Repo containing ansible Playbook to Install Wordpress on docker containers.

I am using a docker container as ansible host and installing wordpress on it.


## Steps

1. Build the image if not already built

```sh
docker build -t diceansible
```

2. Run the docker containers, we are using docker-compose to run 2 containers of the same image. You can also run only one for this lab.

```
docker-compose up -d
```

3. Inspect the server1 container and get the IP.

```
docker inspect <server1-container-name>
```

Copy the IPAddress, it will be in the end.

4. In group_vars/all change the server_hostname to the IP copied from above.

5. Run the Playbook 

```sh
ansible-playbook playbook.yml
```

6. After it runs successfully, copy the container IP and paste in browser, Wordpress should run successfully

