FROM ubuntu:19.10

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y \
    bash \
    git \
    wget \
    curl \
    vim \
    ruby \
    python3-dev \
    python3-pip \
    zsh \
    fish \
    tmux \
    byobu \
    ranger \
    fd-find \
    fzf \
    bat \
    ruby-dev \
    ruby-colorize

# python
RUN pip3 install \
    thefuck

# ruby gems
RUN gem install \
    lolcat \
    tmuxinator \
    colorls

# add non-root user "homer"
RUN useradd -ms /bin/bash homer
USER homer
WORKDIR /home/homer

# Powerline
COPY shared/powerline-install.sh powerline-install.sh
RUN sh powerline-install.sh

COPY shared/powerline-setup.sh powerline-setup.sh
RUN cat powerline-setup.sh >> .bashrc

# colorls
# Nerdfonts (the consuming shell/terminal must have the font installed!)

# reload .bashrc
RUN sh . .bashrc
