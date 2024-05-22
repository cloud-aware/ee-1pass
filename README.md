# ee-1pass
AWX Execution Environment with 1password CLI bundled in

Follow these instructions on how to use Ansible-Builder to create a custom AWX EE Image: https://www.ansible.com/blog/introduction-to-ansible-builder

Build EE image with command:
ansible-builder build --tag ee-1pass --container-runtime docker --verbosity=3  --no-cache

Get the latest docker image id with command:
docker images

Tag the docker image with command:
docker tag <img id from last command> ghcr.io/<github_username>/ee-1pass:latest

Push the docker image to the GitHub container registry with command:
docker push ghcr.io/<github_username>/ee-1pass:latest
