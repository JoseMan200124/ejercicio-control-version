# ejercicio-control-version
JOSÉ DANIEL MAN CASTELLANOS 1020820
# Es una práctica del curso de programación web
flowchart LR
    client[Cliente / Tester] -->|HTTP| ingress[Ingress NGINX demo.local]
    ingress --> service[Service demo-service (ClusterIP)]
    service --> pods[Pods demo-api<br/>(Deployment + HPA)]
    pods --> app[Django + Gunicorn]
    app --> db[SQLite db.sqlite3]
