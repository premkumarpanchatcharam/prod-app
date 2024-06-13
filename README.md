# prod-app
Application deployment.

A. Prepare the applicationset argocd deployment file

guestbook-argocd-applicationset.yaml

1. Used to Configure ApplicationSet on ArgoCD.

2. Update the GKE Application Cluster under the cluster variable and URL variable.

3. Update RepoURL the URL of the repo where application related manifest files exist.

4. Update the Application manifest files location under Path of Source.


B. Create simple guestbook application deployment related guestbook-application-deployment.yaml and guestbook-svc.yaml manifest file for application deployment.

C. Deploy the applicationset using the below kubectl cli.

gcloud container clusters get-credentials prod-app-cluster --zone $ZONE --project $PROJECT_ID

kubectl apply -n argocd -f https://github.com/premkumarpanchatcharam/prod-app/guestbook/guestbook-cd/guestbook-argocd-applicationset.yaml

D. Login into ArgoCD and verify the application is deployed and insyn.

![Uploading image.png…]()


E. if you update the deployment related any config change, the Git sync actions identify the change and push the changes to GKE.
For ex: if you change the replica from 2 and 3 and wait for few min to see the update in the GKE cluser.


   
