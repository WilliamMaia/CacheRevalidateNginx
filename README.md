## Nginx VS NextJs

O NextJS, framework frontend do ambiente node, tem uma excelente estrategia de cache,
e quando isso é unido ao poder de SSG (Gereção de páginas estáticas) 
do framework, dá para ele uma habilidades incríveis.

A estrátegia do nextJS chamada "Revalidate" dá o poder de uma página ser guardada em cache,
e esse cache será revalidado baseado em um parametro de tempo dentro da aplicação. 
Quando uma página é requesitada pelo navegador, essa resposta virá de um arquivo html estático 
que já foi gerado pelo framework, supondo que foi configurado um cache de 60 segundos, então nos próximos
60 segundos, todas as requisições a mesma página serão respondidas com o mesmo arquivo estático gerado anteriormente,
isso permite que durante todo esse periodo em cache o backend e banco de dados não trabalhem, não recebam nenhuma requisição, o que é incrível!

O Nginx pode fazer o mesmo! e melhor...
Qualquer aplicação que gere páginas estáticas pode fazer o mesmo que o NextJS usando o Nginx.
O Nginx é um servidor http e proxy reverso, ele trabalha resolvendo as requisições e comunicando com as aplicações conectadas a ele.

Fiz um exemplo para mostrar como qualquer aplicação, nesse caso uma aplicação Laravel/PHP, pode ter o mesmo comportamento e habilidade de uma aplicação NextJS.