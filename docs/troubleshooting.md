# Trouble shooting 

In this chapter several troubleshootings will be presented. For asking/suggesting of adding one, feel free to raise an issue in the GitHub repository. 

## How to move MesoCraft data folder

When upgrading to a newer version of MesoCraft, it is wanted to move your `work/data` folder as it might contain some custom data you have already changed/created. The following steps need to be performed:
Copy `work/data` subfolder from the old version into the new version (the relative path has to be again `work/data`)
Delete file `work/data/modeling/cache-files/ingredients-cache.bin`. This file will be recreated with the next MesoCraft session.