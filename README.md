
## Этот репозиторий является учебным для освоения основ GO lang и его взаимодействия с Docker  

### Представленный функционал:
1) В директории /binary_hello_world/main представлен исполняемый файл "Hello World": main.go
2) В директории /docker_hello_world/main представлены следующие файлы:  
a) main.go - исполняемый файл "Hello World"  
б) Dockerfile - конфиг-файл для создания docker-image исполняемого файла  
в) Makefile - файл-сборщик программы  

### Инструкция работы с представленным функционалом
I. Для исполнения бинарного "Hello World" файла необходимо:
1) Перейти в директорию с исполняемым файлом main.go:
  

    cd USER_DIR/SBT_GO_diving/binary_hello_world/main
2) Запустить исполняемый файл main.go:


    go run main.go

II. Для работы с docker-сервисом необходимо:
1) Перейти в директорию с файлами конфигурации Docker и исполняемым файлом main.go:


    cd USER_DIR/SBT_GO_diving/docker_hello_world/main
2) Создать образ Docker с именем go-hello-world:


    make build_docker
3) Проверить успешное создание данного образа:


    make check_image_docker
4) Удалить данный образ:


    make clean_up_docker

### Требования к окружению
1) Проверить конфигурацию SDK - GOVERSION
2) Проверить конфигурацию PROXI
3) Проверить расположение файла go.mod относительно GOROOT

Данную информацию можно найти с помощю комманды:


    go env