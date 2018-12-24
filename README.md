# packer-rest-docker
An example repo with using packer to build a docker image with a jar using ansible. 


This is an example repo which uses Packer, Docker and Ansible.
It will use gradle to build a jar which will then be copied across into a docker image using ansible. 
The user can then run the image

Run commands.

```bash
./gradlew build
packer build ./base-packer.json
packer build ./packer.json
docker run -d -p 8080:8080 gerh/test:0.1
curl localhost:8080
```
