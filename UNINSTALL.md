First
you want to stop the instance locate the file in the terminal and use the following command:
```bash
docker compose down
```
Second
To remove all the previous images using the following command:
```bash
docker system prune -a
```
**Warning:** This command will remove all the docker images in your computer, if you use docker for other images than the RegulonDB instance, please use the ```rmi``` command to remove the images one by one
