# gitlab-docker

### 1: `mkdir gitlab`
### 2: `export GITLAB_HOME=$(pwd)/gitlab`
### 3:  `docker-compose up -d`
### 4:  `docker exec -it gitlab-web grep 'Password:' /etc/gitlab/initial_root_password`


`docker exec -it gitlab-runner1 \
  gitlab-runner register \
    --non-interactive \
    --registration-token "P-tC8hy2WMB4NRAS1_bC" \
    --locked=false \
    --description docker-stable \
    --url "http://gitlab.ir" \
    --executor docker \
    --docker-image docker:stable \
    --docker-volumes "/var/run/docker.sock:/var/run/docker.sock" \
    --docker-network-mode gitlab-network`

###5: `sudo vi gitlab/gitlab-runner/config.toml`    
