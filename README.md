# linuxtips-resumo-docker

Este repositório contém anotações sobre o [curso](https://www.youtube.com/playlist?list=PLf-O3X2-mxDkiUH0r_BadgtELJ_qyrFJ_) de Docker fornecido no canal [LinuxTips](https://www.youtube.com/channel/UCJnKVGmXRXrH49Tvrx5X0Sw).
Cada vídeo do curso possuirá uma seção contendo anotações que eu julgar interessantes, porém, nem todos os vídeos do curso serão anotados.
Sinta-se livre para fazer um fork do repositório e/ou propor melhorias em [pull requests](https://help.github.com/articles/using-pull-requests). Bons estudos! :+1::penguin::books:

# Instalação do docker
Siga os passos diretamente em https://docs.docker.com/install/linux/docker-ce/ubuntu/

# Anotações
##### [DESCOMPLICANDO O DOCKER V1 - 01 - O QUE É CONTAINER?](https://www.youtube.com/watch?v=QFuOggpDAOw&index=3&list=PLf-O3X2-mxDkiUH0r_BadgtELJ_qyrFJ_)
- Um container é um processo isolado do sistema que carrega consigo suas dependências.
- É "empacotado" em um arquivo binário.
- Não possui um kernel.
- Utiliza o kernel da máquina host, i.e, a máquina que está executando o container.
- Um container é diferente de uma máquina virtual (VM). Uma VM contém o kernel inteiro do sistema operacional (OS) ao passo que o container contém apenas dados necessários para que o container possa executar a aplicação contida nele.
![Diferença entre uma máquina física, uma VM e um container](https://about.gitlab.com/images/blogimages/containers-vm-bare-metal.png)
- Um container é portável entre máquinas.

##### [DESCOMPLICANDO O DOCKER V1 - 03 - Camadas e o Copy-on-Write](https://www.youtube.com/watch?v=QlpIBEZavzI&list=PLf-O3X2-mxDkiUH0r_BadgtELJ_qyrFJ_&index=5)
- Um container é construído sobre camadas.
- Todas as camadas, exceto a última, são read-only.
- Se um arquivo que está em uma camada read-only precisar ser modificado ele será compiado para a camada superior para que ele possa ser editado. O arquivo original permanece inalterado.
