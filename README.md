# Install-go-protocol-buffers-in-ubuntu
For using golang & GRPC server you need some dependencies in your ubuntu let's update that first

# Download Go in your Downloads Folder
~~~
https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz
~~~

# Install Go by running
~~~
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf Downloads/go1.17.4.linux-amd64.tar.gz
~~~
now, open the <strong>.zshrc</strong> file, and add this in the end
~~~
export PATH=$PATH:/usr/local/go/bin
~~~
save this and run this to check go version
~~~
go version
~~~

# Create go source pages
~~~
mkdir -p go/{src,bin,pkg}
~~~

# Install Protocol Buffers
~~~
sudo apt install -y protobuf-compiler
~~~
then ensure compiler version is 3+
~~~
protoc --version
~~~

# Install proto gen dependency
~~~
go get -u github.com/golang/protobuf/{proto,protoc-gen-go}
~~~
now, open the <strong>.zshrc</strong> file, and add this lines in the end
~~~
export GO_PATH=~/go
export PATH=$PATH:/$GO_PATH/bin
~~~
save this and update ubuntu
~~~
sudo apt-get update
~~~
