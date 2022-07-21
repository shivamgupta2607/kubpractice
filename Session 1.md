* Add all the alias

alias k=kubectl
alias kx='f() { [ "$1" ] && kubectl config use-context $1 || kubectl config current-context ; } ; f'
alias kn='f() { [ "$1" ] && kubectl config set-context --current --namespace $1 || kubectl config view --minify | grep namespace | cut -d" " -f6 ; } ; f'
alias kga="kubectl get all"
export do="--dry-run=client -o yaml"
export kfc="kubectl apply -f"


* . .bashrc -- to execute

* create docker image and tag it with name my-image

docker build -t my-image:v0.1 .

* * save the docker image using docker save
docker save

**Questions:**

1. create a pod inside a namespace after creating 

k create ns pod-namespace
kn pod-namespace
-- k run is used to create a pod
k run pod-1 --image=nginx $do > q2.yaml

--container name can not be set from command line

edit the q2.yaml to rename container

create the resources from file

$kfc q2.yaml -- kubectl apply -f q2.yaml

kubectl get pods -w


2. persisitent volume

in the cheatsheet search "pv pvc pod"

change the desired configuration
Get commands

k get pv
k get pvc




