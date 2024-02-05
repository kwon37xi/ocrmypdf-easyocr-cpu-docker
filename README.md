dock# ocrmypdf-easyocr-cpu-docker
ocrmypdf with easyocr docker

```
git clone https://github.com/kwon37xi/ocrmypdf-easyocr-cpu-docker.git

docker build --file Dockerfile.easyocr-cpu --tag ocrmypdf-easyocr .

alias ompe='docker run --rm -i --user "$(id -u):$(id -g)" --workdir /data -v "$PWD:/data" -e HOME=/data ocrmypdf-easyocr'

ompe -l kor+eng--deskew --clean --optimize 3 --easyocr-workers <CPU갯수> --easyocr-no-gpu /data/<input>.pdf /data/<output.pdf>
```
