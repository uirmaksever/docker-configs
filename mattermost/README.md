This repository contains the docker-compose and Dockerfile files to run Mattermost on Raspberry Pi as a docker stack. [ubiquitous-memory](ubiquitous-memory) repository publishes built tar files of Mattermost for arm64 architecture. However, last release published by them was on 7.5.2 as of April 2023, and the most recent Mattermost version is 7.10. [In this pull request](https://github.com/SmartHoneybee/ubiquitous-memory/pull/162), maintainer of ubiquitous-memory has mentioned that he is not actively maintaining the repository. I was planning to use Mattermost for Boards (Focalboard), but it is still installable as a plugin on 7.5.2.


Build the image by 'docker-compose up -d --build'

After running the container, it should have created necessary files under 'volumes' folder. Run the following command to fix permissions.
'''
sudo chown -R 2000:2000 ./volumes/app/mattermost
'''