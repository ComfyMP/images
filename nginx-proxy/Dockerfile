FROM nginxproxy/nginx-proxy
RUN { \
      echo 'server_tokens off;'; \
      echo 'client_max_body_size 10g;'; \
    } > /etc/nginx/conf.d/custom.conf