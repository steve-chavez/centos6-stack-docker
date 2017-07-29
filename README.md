# centos6-stack

Centos 6 image with postgresql 9.3 client libs for stack builds.

## Usage:

In your project directory: 

```bash 
docker run -it --rm -v $(pwd):/source stevechavez/centos6-stack <stack_command>
``` 

## For building and obtaining a binary:

```bash 
docker run -it --rm -v $(pwd):/source -v /tmp/bin:/root/.local/bin/ \
           stevechavez/centos6-stack build --copy-bins --install-ghc
# -v /source/.stack-work can be added to ignore the host .stack-work
# -v $HOME/.stack:/root/.stack can be added to cache dependencies on the host
# After this the binary will be in /tmp/bin
``` 
