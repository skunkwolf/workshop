# Use the official Go image as a base
FROM golang:1.21

# Set the working directory inside the container
WORKDIR /app

# Install zsh and other necessary tools
RUN apt-get update \
    && apt-get install -y zsh \
    && rm -rf /var/lib/apt/lists/*

# Install the necessary Go tools
RUN go install golang.org/x/tools/gopls@latest \
    && go install golang.org/x/tools/cmd/goimports@latest \
    && go install github.com/rogpeppe/godef@latest \
    && go install github.com/ramya-rao-a/go-outline@latest \
    && go install github.com/go-delve/delve/cmd/dlv@latest \
    && go install github.com/golangci/golangci-lint/cmd/golangci-lint@v1.42.0
