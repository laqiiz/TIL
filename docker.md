# Docker

## frequency commands
```
# when want to research in ubuntu
docker run -it ubuntu /bin/bash
```

## Actually I made a mistake

* CMD in Dockerfile

```sh
CMD ["./main", "--host 0.0.0.0"]
↓↓↓
unknown flag `host 0.0.0.0'

CMD ["./main", "--host", "0.0.0.0"]
↓↓↓
OK
```
