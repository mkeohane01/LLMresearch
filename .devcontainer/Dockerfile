FROM python:3.8

# Set up non-root user, if needed
ARG USERNAME=mkeohane01
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN addgroup --gid $USER_GID $USERNAME \
    && adduser --disabled-password --gecos "" --uid $USER_UID --gid $USER_GID $USERNAME

# Set up working directory
WORKDIR /workspace

# Ensure Python 3.8 is the default
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1

# Optional: Install additional packages or dependencies
# RUN apt-get update && apt-get install -y <package-name>

# Optional: Set up a virtual environment
# RUN python3 -m venv /workspace/venv
# ENV PATH="/workspace/venv/bin:$PATH"

# Set VS Code user permissions
RUN chown -R $USERNAME:$USERNAME /workspace

# Switch to non-root user
USER $USERNAME
