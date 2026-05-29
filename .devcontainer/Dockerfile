FROM bretfisher/jekyll-serve:stable-20260414-2a8cdc9

ENV BUNDLE_PATH="/home/jekyll/.bundle-gems"

# https://code.visualstudio.com/remote/advancedcontainers/add-nonroot-user
ARG USERNAME=jekyll
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create the user
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

USER $USERNAME
