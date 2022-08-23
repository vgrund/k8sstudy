Um estudo de Kubernetes
=

Este documento é uma compilação do estudo feito sobre o funcionamento do K8S e pode apresentar conceitos incompletos, inconsistentes, ou incorretos.

>### O que é o Kubernetes?  
>
> Kubernetes ou K8S, é um sistema open source para automação, gerencia, escalabilidade e deploy de aplicações baseadas em containeres.
> 

Nas minhas palavras:
K8S é um sistema de gerenciamento, escalabilidade e deploy de sistemas distribuidos baseados em containeres.

K8S foi criado por 3 engenheiros do Google e é sucessor de projetos mais antigos, Borg e Omega.

>### Qual a diferença entre VM e K8S?  
>
>ifjsdif
>

## A anatomia de cluster K8S

![](./images/Kubernetes-4.jpeg)

>### Quais são os principais objetos do K8S?  
>
> K8S possui um conjunto de objetos com funções 
>

>### O que é um Pod?  
>
> Pods são a menor estrutura possível, ou a menor estrutura publicavel do K8S. Ele é a abstração para um processo rodando no cluster, podemos entende-lo como um agrupador de containeres, embora a recomendação é que cada Pod tenha apenas um container.  
>Um Pod é efemero, isto é, ele é considerado uma unidade totalmente descartavel do K8S. Todo o trabalho feito pelo pod ou no pod só se mantem nele até que seja removido, então tudo é perdido.
>

>### O que é Service?  
>
> Assim como o Pod, Service é uma abstração, porem de rede. Definem um conjunto lógico de pods e uma politica pela qual saberemos como vamos acessa-los. 
![](./images/Kubernetes-5.png)
> Como pods são efemeros, os IPs fatalmente irão mudar, então acessamos nossas aplicações atraves dos Services que possuem IP fixo.  
> Services implementam Label Selectors que é o artificio usado para agrupar os pods.
> Existem algumas práticas recomendadas para definição dessas Labels:
> * Definir ambiente: env=prod
> * Versionamento: version=1.2.1
> * Nome do serviço: app_name=api-livros
> * Agrupamento de projetos: project=api-containers
![](./images/Kubernetes-6.png)
>

>### O que é Deployment?  
>
>

>### O que é ReplicaSet?  
>
>

>### O que é HPA?  
>
>

>### O que é Namespace?  
>
>

>### O que é Ingress?  
>
>

>### Quais são os tamanhos possíveis de CPU e Memória?  
>
>

>### O que é Helm e pra que serve?  
>
>
