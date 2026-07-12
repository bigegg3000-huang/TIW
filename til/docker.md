docker build -t rsactftool/rsactftool .

docker run -it --rm -v $PWD:/data rsactftool/rsactftool <arguments>

docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
