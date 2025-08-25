🎮 Deploy Tetris Game on Kubernetes using Argo CD

In this project, I demonstrate step by step how I deployed a Tetris game on Kubernetes using GitOps with Argo CD.


---

🛠 Prerequisites

Before starting, I made sure I had:

A running Kubernetes cluster (Minikube, Kind, or a managed cluster)

kubectl installed and configured

Argo CD installed in the cluster

A Git repository containing the Kubernetes manifests for the Tetris game

Basic understanding of GitOps concepts

Browser access to check the game once deployed



---

🚀 Step 1: Install Argo CD

1. I created a dedicated namespace for Argo CD.


2. Installed Argo CD using the official manifests.


3. Exposed the Argo CD server and logged in with the initial admin credentials.


4. Opened the Argo CD dashboard in my browser.




---

🎮 Step 2: Prepare the Tetris Application

1. I used a pre-built container image of the Tetris game.


2. Created Kubernetes manifests.


3. Pushed these manifests into my Git repository under a folder named manifests/.


4. Ensured the repository was accessible to Argo CD.


5. Validated manifests locally before pushing them.




---

🔗 Step 3: Connect Repository to Argo CD

1. I logged in to the Argo CD dashboard.


2. Added my Git repository containing the Tetris manifests.


3. Verified that Argo CD could read the manifests successfully.


4. Confirmed connectivity and repository health inside Argo CD.




---

📦 Step 4: Create Argo CD Application

1. I created a new application in Argo CD.


2. Set the repository URL and the path to the manifests.


3. Specified the destination namespace and Kubernetes cluster.


4. Enabled automated sync with self-heal and prune options.


5. Saved and verified the application definition.




---

✅ Step 5: Deploy the Tetris Game

1. I synced the application from the Argo CD dashboard.


2. Waited until the application was shown as Healthy and Synced.


3. Confirmed that the Tetris pods and services were running in the cluster.


4. Verified no errors appeared in pod logs during startup.




---

🌐 Step 6: Access the Game

1. Since I used a NodePort service, I accessed the game through the node IP and port.


2. Verified that the Tetris game was up and playable in the browser.


3. Shared the game link to demonstrate the deployment.




---

🔄 Step 7: GitOps Workflow in Action

1. I made changes to the Kubernetes manifests in my Git repository.


2. Committed and pushed the updates.


3. Argo CD detected the changes and automatically applied them to the cluster.


4. Verified the update in the Argo CD dashboard.


5. Observed how Argo CD maintained cluster state in sync with Git.




---

📊 Step 8: Monitor and Manage

1. I monitored application health and sync status from the Argo CD dashboard.


2. Checked pod logs with kubectl for troubleshooting.


3. Tested rollback features directly from Argo CD.


4. Monitored resource usage (CPU/Memory) for deployed pods.


5. Used Argo CD’s history view to track changes over time.




---

🧹 Step 9: Cleanup

1. I deleted the Tetris application from Argo CD.


2. Removed the Tetris-related Kubernetes resources from the cluster.


3. Optionally, uninstalled Argo CD if it was only used for this demo.


4. Cleaned up my Git repository branches used for testing.



By performing cleanup, I ensured my Kubernetes cluster stayed optimized and ready for other projects.


---

📝 Conclusion

This project shows how I successfully deployed a Tetris game on Kubernetes using Argo CD with a GitOps approach. The process was automated, version-controlled, and reliable. Cleanup at the end of the process was crucial to keeping the environment tidy and efficient.

Through this project, I gained hands-on experience in:

Setting up Argo CD for GitOps workflows

Managing deployments through Git commits

Observing automated synchronization in action

Understanding rollback and self-healing in Kubernetes

