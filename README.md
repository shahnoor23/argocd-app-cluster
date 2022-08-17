# argocd-app-cluster


App Of Apps Pattern

Step1: Configure Child applications. In this repo I have create two simple deployment file of nginx "deployments/app-1/app-1.yaml" and "deployments/app-2/app-2.yaml". Its a simple manifest file. Now that your Manifest files are ready, you must create Argo CD Applications pointing to those Manifests.


Step2: Now create two sample application of argocd i.e argocd-app/app-1.yaml and argocd-app/app-2.yaml. As you can see, you are creating a Kubernetes object called Application in different namespaces. This object contains the source Git repository and destination server details. Your Applications are pointing to the Nginx manifest files you created earlier.


Step3: Presently you would like a few way to tell Argo CD how to discover your Nginx applications. Do this by making however another Application. This design is called the App of Apps design, where one Application contains the enlightening to convey numerous child Applications.
Create from GUI a new app with pointing to the folder "argocd-app". Once it has been created, begins syncing in the GUI.



