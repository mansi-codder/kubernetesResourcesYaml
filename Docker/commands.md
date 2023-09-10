docker build -t ubuntu-sleeper .

# this will update the sleep from 5 to 10 
# docker run image-name <command to append after entrypoint>
docker run ubuntu-sleeper 10

# command to override entrypoint 
docker run --name=my-ubuntu-sleeper --entrypoint sleep2.0 --image= ubuntu-sleeper 10
