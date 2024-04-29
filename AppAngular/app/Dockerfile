#########################################-Con nginx puerto 80-###########################################


#FROM node AS angular

#WORKDIR /app

#COPY package*.json ./
#RUN npm install 
#RUN npx ngcc --properties es2023 browser module main --first-only --create-ivy-entry-points
#COPY . .

#RUN npm run build


#FROM nginx:stable
#COPY --from=angular /app/dist/app/browser /usr/share/nginx/html
#EXPOSE 80



#########################################-Sin nginx puerto 4200-###########################################

FROM node:alpine as angular

WORKDIR /app

COPY . /app

RUN npm install -g @angular/cli

RUN npm install

CMD ["ng", "serve", "--host", "0.0.0.0"]


