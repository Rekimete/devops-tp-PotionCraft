FROM nginx:alpine

# Copy frontend static files into nginx html folder
COPY . /usr/share/nginx/html

# Expose port 80 (container)
EXPOSE 80

# Start nginx in foreground
CMD ["nginx", "-g", "daemon off;"]

