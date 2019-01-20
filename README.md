# Sérgio da Victori 

(sergiodavictoria@hotmail.com)

# Instalação do Minishift(OpenShift OKD(Origin) Single Cluster
OKD: Renaming of OpenShift Origin with 3.10 Release Kubernetes 1.10


RECOMENDADO 16 GB RAM Linux (Centos, Fedora, Ubuntu etc..Ou Mac), no meu caso estou usando, CentOS Linux release 7.6.1810 (Core).

Primeiro temos que ter um hypervisors(KVM) o cluster do minishift roda sobre o (KVM), estou uando o VirtualBox veja como instalar (https://wiki.centos.org/HowTos/Virtualization/VirtualBox)


Instalando o minishift minishift-1.30.0

Vamos dar inicio a instalação, faça download do minishift 1.3
wget https://github.com/minishift/minishift/releases/download/v1.30.0/minishift-1.30.0-linux-amd64.tgz

Descompactando o tgz
tar xvzf  minishift-1.30.0-linux-amd64.tgz

# Parameters

* --vm-driver=virtualbox      (Define hypervisors) neste caso,  Virtual Box
* --cpus=4                    (Quantidade de CPU)
* --memory=12000              (Quantidade de Memória)
* --disk-size 70g             (Espaço em Disco)

# run
./minishift start --vm-driver=virtualbox --cpus=4 --memory=12000 --disk-size 70g


# Defina a variavel de ambiente
Verificando o path, depois devemos fazer um append nas variáveis de ambiente
execute ./minishift oc-env
Não esqueça de coloar no path da sua máquina /home/user/.minishift/cache/oc/v3.11.0/linux

# Copia do binário
cp minishift /home/user/.minishift/cache/oc/v3.11.0/linux

# Executando o console 
carregando o console mininishift console

# Feito
Pronto minishift instaldo, agora é so começar a Desenvolver
