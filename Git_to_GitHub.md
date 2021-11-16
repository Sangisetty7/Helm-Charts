**Step-1:**  
Create and Package helm chart as shown below.
```
helm create nginx     # nginx will be created.
helm package nginx    # nginx will be packaged "nginx-0.1.0.tgz" .
```
**Step-2:**  
Log into Github and create a repository. I am choosing "helm_demo" as an example. Go to the created repository and copy the HTTPS Git link which you can find under code.
**Step-3:**  
Open your terminal and clone the copied repository "helm_demo" as shown below
```
git clone https://github.com/<username>/helm_demo.git     #Modify the username.
```
**Step-4:**  
Now follow the below procedure
```
ls                         # Chech whether repo was cloned or not. You can see helm_demo directory.
cd helm_demo               # Change directory.
git branch                 # You will be in the master/main branch.
git checkout -b gh-pages   # I am creating another sub-branch called "gh-pages" where I will create an index.yaml file.
cp ../nginx-0.1.0.tgz .    # Copying the helm package to gh-pages branch .
helm repo index .          # Creating index.yaml file.
git add .                  # Adding the files to git.
git commit -m 'commiting'  # Commiting the changes in the branch.
git push origin gh-pages   # Pusing the changes to GitHub.
```
**Step-5:** 
Navigate to GitHub and Check whether the branch "gh-pages" have all the modifications done. Check the repository settings 

**Step-6:**
Now we will commit the changes of "gh-pages" branch to "master" branch. I am using terminal to do changes.
```
helm repo add helm_demo  <repo adress>    # repo-address can be found at settings
helm search repo helm_demo                # You can find the helm charts 
helm fetch <chart>                        # Using this you can fetch the charts and use for deployment purpose.
```



