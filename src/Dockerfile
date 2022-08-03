#imagem base:versao da imagem, garantindo deste modo a idempotência
FROM node:16.1.0 


# directorio de trabalho, semelhante ao mkdir e cd 
WORKDIR /app 

COPY package*.json ./

RUN npm install # baixando os pacotes para a imagem
# copiando os restantes arquivos
COPY . .  
# a porta que a aplicacao esta ouvindo
EXPOSE 8080

# comando de inicializacao do container
CMD ["node","server.js"]

# docker build -t cabicho/conversao-temperatura:v1 .
# docker run -d -p 8080:8080 cabicho/conversao-temperatura:v1
