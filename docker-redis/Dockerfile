FROM node:10-alpine 
#versão de uma máquina com o básico do node versão 10

WORKDIR /usr/app 
#Aonde vai ser descarregada a imagem da nossa app dentro da máquina

COPY package.json yarn.lock ./ 
#copiar os arquivos

RUN npm 
#executa o yarn para instalar as dependências

COPY . .

EXPOSE 3000 
#Vai colocar a porta 3000 exposta

CMD [“yarn”, “start”] 
#vai rodar o comando yarn buscando o valor do start, configurado no package.json
