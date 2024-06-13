# prod-app
Application deployment.
File Name	Usage	Remarks
guestbook-argocd-applicationset.yaml	"1. Used to Configure ApplicationSet on ArgoCD.
2. Update the GKE Application Cluster under the cluster variable and URL variable.
3. Update RepoURL the URL of the repo where application related manifest files exist.
4. Update the Application manifest files location under Path of Source.

"	
guestbook-application-deployment.yaml	Guestbook App deployment manifest	
guestbook-svc.yaml	Guestbook App service manifest file	
![Uploading image.png…]()
