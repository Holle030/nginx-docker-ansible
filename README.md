# Nginx Docker Ansible Deployment 🚀

Ein Beispielprojekt für automatisiertes Deployment mit Docker und Ansible.

## 📁 Projektstruktur
```
nginx-docker-ansible/
├── docker/
│   ├── Dockerfile         # Nginx Container Definition
│   ├── docker-compose.yml # Container Orchestration
│   └── html/             # Website Dateien
├── ansible/
│   ├── playbook.yml      # Deployment Automation
│   └── inventory.ini     # Server Liste
└── README.md
```

## 🛠️ Voraussetzungen

- Docker & Docker Compose
- Ansible
- Git

## 🚀 Schnellstart

### 1. Repository klonen
```bash
git clone <repo-url>
cd nginx-docker-ansible
```

### 2. Manuell mit Docker starten
```bash
cd docker
docker-compose up -d
```
Website erreichbar unter: http://localhost:8080

### 3. Mit Ansible deployen
```bash
cd ansible
ansible-playbook -i inventory.ini playbook.yml
```

## 📝 Was macht das Projekt?

- **Docker**: Containerisiert eine Nginx Webserver Instanz
- **Ansible**: Automatisiert das Deployment auf lokale/remote Server
- **Website**: Simple HTML Seite als Beispiel-Content

## 🔧 Anpassungen

### Website ändern
Bearbeite `docker/html/index.html`

### Port ändern  
In `docker/docker-compose.yml`:
```yaml
ports:
  - "DEIN_PORT:80"
```

### Remote Server hinzufügen
In `ansible/inventory.ini`:
```ini
[webservers]
server1 ansible_host=192.168.1.100 ansible_user=ubuntu
```

## 📚 Gelernte Konzepte

- Git Versionierung
- Docker Containerisierung
- Docker Compose für Multi-Container
- Ansible für Infrastructure as Code
- Playbook Entwicklung

## 🐛 Troubleshooting

**Docker Permission Denied:**
```bash
sudo usermod -aG docker $USER
newgrp docker
```

**Container Name Konflikt:**
```bash
docker rm -f nginx-website
```

## 📖 Nächste Schritte

- [ ] SSL/HTTPS hinzufügen
- [ ] CI/CD Pipeline einrichten
- [ ] Monitoring (Prometheus/Grafana)
- [ ] Load Balancing
- [ ] Kubernetes Migration

## 👤 Autor
Holle030
