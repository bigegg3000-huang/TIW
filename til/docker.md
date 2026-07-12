docker build -t rsactftool/rsactftool .
docker run -it --rm -v $PWD:/data rsactftool/rsactftool <arguments>
