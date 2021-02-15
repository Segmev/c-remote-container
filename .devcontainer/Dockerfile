FROM gcc:latest

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
ARG PW=docker

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && echo 'alias ls="ls --color"' >> /root/.bashrc \
    && echo 'alias ls="ls --color"' >> ~/.bashrc


COPY . /workspaces/Cshell

USER ${UID}:${GID}
WORKDIR /workspaces/Cshell
