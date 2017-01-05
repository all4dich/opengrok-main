# opengrok-main
Make a opengrok instance with a independent web context path 

## What to do
1. Make a new :open_file_folder:**OPENGROK_INSTANCE_BASE** folder for a web context
  1. Sub folders
    1. :open_file_folder:**OPENGROK_INSTANCE_BASE/src**
    1. :open_file_folder:**OPENGROK_INSTANCE_BASE/data**    
1. Make a web application file witch a web context and :open_file_folder:**OPENGROK_INSTANCE_BASE** location
1. Deploy an web app to TOMCAT
1. If you define :pencil2:*$GIT_BRANCH* and :pencil2:*$GIT_URL*, clone it under :open_file_folder:**OPENGROK_DISTRIBUTION_BASE/src** and create indexed data

## Make a OpenGrok instance with a web application name.
1. Clone this project into a local. Set it as :open_file_folder:**OPENGROK_DISTRIBUTION_BASE**
1. Add Tomcat's :open_file_folder:**bin** folder's absolute path to :pencil2:*$PATH*
1. Run :pencil:**$OPENGROK_DISTRIBUTION_BASE/bin/run.sh**
  * If you need some files, please write it on a file and set it with **OPENGROK_CONFIGURATION**
  * run.conf
  ```shell
  IGNORE_PATTERNS="-i .git -i */downloads -i */temp/*.i"
  OPENGROK_FLUSH_RAM_BUFFER_SIZE="-m 256 -T 120"
  ```
    * Command
  ```shell
  OPENGROK_CONFIGURATION=./run.conf $OPENGROK_DISTRIBUTION_BASE/bin/run.sh
  ```
1. Check a web app's url on a browser