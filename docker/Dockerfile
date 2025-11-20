FROM nginx:alpine

# Arbeitsverzeichnis
WORKDIR /usr/share/nginx/html

# Kopiere Website-Dateien (erstellen wir gleich)
COPY ./html /usr/share/nginx/html

# Port freigeben
EXPOSE 80

# Nginx starten
CMD ["nginx", "-g", "daemon off;"]
