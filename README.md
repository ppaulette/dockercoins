# dockercoins
```
github_branch=2021-10
github_repository=dockercoins
github_username=academiaonline
```
```
git clone https://github.com/${github_username}/${github_repository}
cd ${github_repository}/
git checkout ${github_branch}
```
```
for app in hasher rng webui worker
do
  docker build --file ${app}/Dockerfile --tag ${github_username}/${github_repository}:${github_branch}-${app} .
done
```
```
for app in hasher redis rng
do
  docker network create ${app}
done
```
