# Based on: https://github.com/microsoft/vscode-dev-containers/tree/v0.166.1/containers/python-3/.devcontainer/base.Dockerfile
FROM lambda-stack:20.04

# [Optional] If your pip requirements rarely change, uncomment this section to add them to the image.
COPY .devcontainer/requirements.txt /tmp/pip-tmp/
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt \
   && rm -rf /tmp/pip-tmp
# ENV PATH="$HOME/.local/bin:$PATH"

COPY .devcontainer/google-drive-api.py /tmp/google-drive/
# RUN python3 /tmp/google-drive/google-drive-api.py

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends wget

# ZSH install. Default powerline10k theme, no plugins installed
RUN sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.1.1/zsh-in-docker.sh)"