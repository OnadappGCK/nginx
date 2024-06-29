# Utiliser une image Nginx pour servir l'application
FROM nginx:alpine

# Créer les répertoires nécessaires et définir les permissions
RUN mkdir -p /usr/share/nginx/html/app && \
    mkdir -p /tmp/client_temp && \
    mkdir -p /tmp/proxy_temp && \
    mkdir -p /tmp/fastcgi_temp && \
    mkdir -p /tmp/uwsgi_temp && \
    mkdir -p /tmp/scgi_temp && \
    chmod -R 777 /tmp

# Copier la configuration Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Exposer le port 80
EXPOSE 80

# Lancer Nginx
CMD ["nginx", "-g", "daemon off;"]