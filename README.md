# Portainer
Docker için arayüz uygulaması

# konteyner çalıştırmadan önce onu kalıcı hale getirmek için Docker birimi oluştur. Bu birim tüm kapsayıcı bilgileni içerir ve onu kalıcı tutar.
$ docker volume create portainer_data

$ docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
