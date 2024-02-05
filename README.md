dock# ocrmypdf-easyocr-cpu-docker
ocrmypdf with easyocr docker

```
git clone https://github.com/kwon37xi/ocrmypdf-easyocr-cpu-docker.git

docker build --file Dockerfile.easyocr-cpu --tag ocrmypdf-easyocr .

alias ompe='docker run --rm -i --workdir /data -v "$PWD:/data" ocrmypdf-easyocr'

ompe -l kor+eng--deskew --clean --optimize 3 /data/<input>.pdf /data/<output.pdf>
```
