# machinelearningwithgo

Learning ML from "Machine Learning With Go" by Daniel Whitenack

https://www.packtpub.com/big-data-and-business-intelligence/machine-learning-go?utm_source=github&utm_medium=repository&utm_campaign=9781785882104


---
### Installation
* Go (go version go1.10 darwin/amd64)
* Source code from the book
    * https://github.com/PacktPublishing/Machine-Learning-With-Go
    * Note: The source code is in a local Go directory.
* Docker 
* Tensorflow (runs on Docker)
    * https://www.tensorflow.org/install/
* Minikube (Kubernetes)
    * https://kubernetes.io/docs/getting-started-guides/minikube/
    * https://github.com/kubernetes/minikube
    * https://github.com/kubernetes/minikube/releases
    * Hypervisor - do I need this?
    * kubectl
        * Mac
            * brew install kubectl
        * Linux
            * ...
    * Minikube
        * Mac
            * curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.26.1/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
            * brew cask install minikube
        * Linux
            * curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.26.1/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
* Pachyderm (runs on Minikube)
    * http://pachyderm.readthedocs.io/en/latest/index.html
    * pachctl
        * Mac
            * brew tap pachyderm/tap && brew install pachyderm/tap/pachctl@1.7
        * For Debian based linux (64 bit) or Window 10+ on WSL:
            * curl -o /tmp/pachctl.deb -L https://github.com/pachyderm/pachyderm/releases/download/v1.7.1/pachctl_1.7.1_amd64.deb && sudo dpkg -i /tmp/pachctl.deb
* Jupyter (not part of the book)


---
### Start and stop things
* Tensorflow
    * docker run -it tensorflow/tensorflow bash
    * docker run -it -p 8888:8888 tensorflow/tensorflow
        * To run in a Jupyter notebook
* Minikube
    * minikube [delete|start|stop]
* Pachyderm
    * minikube delete
    * minikube start
    * pachctl deploy local
    * Check its status with "kubectl get all"
    * Port forwarding "pachctl port-forward &"
    * localhost:30080


---
### Pachyderm
* data versioning
* runs on K8S