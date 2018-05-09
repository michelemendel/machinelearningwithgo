# machinelearningwithgo

Learning ML from "Machine Learning With Go" by Daniel Whitenack

https://www.packtpub.com/big-data-and-business-intelligence/machine-learning-go?utm_source=github&utm_medium=repository&utm_campaign=9781785882104


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
* NOT YET INSTALLED: Pachyderm (runs on Minikube)
    * http://pachyderm.readthedocs.io/en/latest/index.html
* Jupyter (not part of the book)

### Start and stop things
* Tensorflow
    * docker run -it tensorflow/tensorflow bash
    * docker run -it -p 8888:8888 tensorflow/tensorflow
        * To run in a Jupyter notebook
*  Minikube
* Pachyderm