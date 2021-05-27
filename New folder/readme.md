**Structure**

REPO(FEATURE NAME)
    
    |---->feature_site1_hardware
    
        |---->readme.json
        |---->weights.h5
        |---->weights_config.cfg
    |---->feature_site1_hardware2
        |....

    |---->feature_site2_hardware
    |---->feature_site3_hardware


Helmet_weights (repo)

    |---->master
          |---->readme.md
    |---->helmet_generic_gpu
          |---->readme.md
          |---->weight_file.h5
          |---->weight_config.cfg
    |---->helmet_generic_openvino
          |---->readme.md
          |---->weight_file.h5
          |---->weight_config.cfg
    |---->helmet_ang
          |---->readme.md
          |---->weight_file.h5
          |---->weight_config.cfg


# DESCRIBING THE STRUCTURE
1. The repo corresponds to particular feature such as helmet,mask,ANPR.
2. The repo consists of a master branch with readme file explaining schema for the repo.
3. The repo consists of several other branches in the format : feature_sitename_hardware
    where each sitename can have mulitiple hardwares such as helmet_ang_gpu , helmet_ang_openvino etc...
4. Each branch contains readme.json having details related to the weight file, a weight gile and a config file.

## STEPS FOR CREATING A SIMILAR REPO 
1. Create a repo with a feature name and add this readme.md. ( eg-helmet_weights)
2. For creating multiple branches of the format feature_sitename_hardware ( eg- helmet_generic_gpu):
    1. Go to the helmet_generic folder on the system with all the files. 
    2. Initialse git and dvc and follow the mentioned steps to push the git and dvc repo with weight pointers.
    https://github.com/DeepSightAILabs/dvc/blob/master/README.md
3. For creating other branches in the same repo follow the same steps as mentioned above.
