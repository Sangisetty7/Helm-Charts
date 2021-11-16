**Step-1:**  Create and Package helm chart as shown below.
```
helm create nginx 
helm package nginx
```
**Step-2:**  Log into Github and create a repository.


1.master or main
2.gh-pages
Step 2 Once you create a new repository, then under code section you can able to find the HTTPS Git clone URL copy that and clone from terminal. command git clone now you can able to see the repo name as a directory at pwd cd < repo directory >

Step 3 need to switch to gh-pages by using git checkout gh-pages now copy that package .tar file to here now we need an index file to access this helm

helm repo index .
git add .
git commit -m 'updates'
git push -u origin gh-pages
Step 4 Now go to your repo settings and change the settings called 'Pages settings now has its own dedicated tab' use the gh-pages branch and save. You have successfully added your helm package to github you can add those repo in your local helm

helm repo add <repo address> 
the repo address will appear at GitHub pages settings where you have changed the default branch from main to gh-pages step 1

Step 5 Now the back end we have complerd to display the yaml templates on main branch need to switch to the main branch

helm checkout master
now copy the helm repo to pwd

git add .
git commit -m 'updates'
git push -u origin master
