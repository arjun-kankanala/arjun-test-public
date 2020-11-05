# elvis-dif-talend
Talend Data Integration ETL

## Run Maven Build for the project
Login to dev server and pull your 'feature branch' where you made the changes

Run the build on dev server for any changes to the project and prior to creating the pull request

Note: Modify the "-pl" in maven command to build the artifacts for jobs stated in buildJobs.csv

$ sudo mvn -X -e install \\
-f //home/arjun.ka/repos/elvis-dif-talend/ELVIS_DIF_TALEND/poms/pom.xml \\
-pl jobs/process/DIF/NORMALIZATION/dif_normalization_processor_0.1,jobs/process/DIF/LOAD/DATABASE/dif_load_database_norm_v2_0.1,jobs/process/DIF/LOAD/DATABASE/dif_load_database_v2_0.1,jobs/process/DIF/LOAD/DATABASE/dif_load_database_parent_v2_0.1 \\
-s /home/svcdedev/talend_prototype/settings-m2repo-old.xml \\
-Dlicense.path=/home/svcdedev/TalendStudio-7.3.1/studio/license \\
-Dproduct.path=/home/svcdedev/TalendStudio-7.3.1/studio \\
-DforceUpdate=true \\
-Dgeneration.type=local

## Once the build is successfull, create a pull request to merge your feature branch to the development branch

