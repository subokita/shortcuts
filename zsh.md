* Generate ISO-8601 compliant date

```
date -u +"%Y-%m-%dT%H:%M:%SZ"`          # Generate current date-time using specific fofrmat
```

* Generate UUID4 in lower case

```
uuidgen | tr "[:upper:]" "[:lower:]     # Generate UUID4 and translate upper to lower case
```

* Monitoring changes in directory

```
brew install watch      # or apt-get install if it's possible
watch -n 0.5 'ls'       #  basically ls current directory for every half second
```


* List the size of all the directories and fiels

```
brew install coreutils  # Just to install gsort
du -sh * | gsort -h     # Run disk usage and sort it in human readable manner
```


* Aliases to remove docker containers, volumes, images, networks (put these in your .bashrc or .zshrc )

```
alias docker-remove-containers="docker ps -a | awk 'NR!=1 {print \$1}' | xargs docker rm -f"
alias docker-remove-images="docker images | awk 'NR!=1 {print \$3}' | xargs docker rmi -f"
alias docker-remove-networks="docker network ls | awk 'NR!=1 {print \$1}' | xargs docker network rm"
alias docker-remove-volumes="docker volume ls | awk 'NR!=1 {print \$2}' | xargs docker volume rm"
```