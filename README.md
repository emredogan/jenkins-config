# Jenkins Configuration File

`config.xml` file represents an example settings for Jenkins for an Android project.

Configuration has the following settings:

- Job is parameterized for the branch so user can enter which branch to build from. (Default is master)

- Jenkins job is triggered everytime user pushes his code or after the pull request.

- Build has the following tasks.
  - Run unit tests
  - Sign and create an release apk (Keystore files and values are safely stored on Jenkins)
  - Upload it as an artifact to Jenkins
 
- If build is successful:
  - Upload it to the Google Play Alpha channel.
- Otherwise: 
  - Send email to the developers together with the build log.
