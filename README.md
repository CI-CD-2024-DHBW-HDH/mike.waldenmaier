# Klausur 2023 DHBW HDH

## Setup

### Klone dieses Repository

1. Klone das Repository
   ```bash
   git clone <TODO repo url>
   cd klausur
   git remote remove origin
   ```
2. Erstelle in der GitHub Organisation ein Repository mit dem Namen **\<vorname>.\<nachname>**
3. Lade den Stand in das Repository hoch
   ```bash
   git remote add origin <url deines Repositories>
   git push -u origin master
   ```
4. Erstelle einen Branch für die Bearbeitung
   > Vergesse am Ende nicht deine Bearbeitung hochzuladen

### Sicherstellen, dass alles geht

Führe folgende Befehle in deinem Repository aus, um sicherzustellen, dass alles geht:

```bash
npm install

npm run dev
```

## Aufgaben (20 Punkte)

1. Installiere: **(3 Punkte)**

   - ESLint
   - Jest
   - Prettier
     > Die Config Dateien brauchen nicht angepasst werden

   > Denke auch an die nötigen Typescript dependencies

2. Schreibe ein `Dockerfile`, dass dazu benutzt werden kann, die Seite zur Verfügung zu stellen **(2 Punkte)**
3. Schreibe GitHub Actions für: **(3 Punkte)**
   - Continuous Integration
   - Continuous Delivery (GitHub Packages)
   - Continuous Deployment (GitHub Pages)
4. Definiere alle nötigen Manifeste um das erstellte Image auf einem Kubernetes Cluster zu deployen **(5 Punkte)**
5. Erkläre in eigenen Worten:

   - Welche Vorteile ein Kubernetes Deployment gegenüber einem Kubernetes Pod hat **(2 Punkte)**

   `Ein Kubernetes Deployment ist eine höhere Abstraktion als ein Pod. Es erlaubt das einfache Skalieren und Aktualisieren von Anwendungen. Ein Deployment definiert die gewünschte Anzahl an Pods und sorgt dafür, dass diese Anzahl auch vorhanden ist. Ein Deployment kann auch die Anzahl der Pods anpassen, wenn die Last auf der Anwendung steigt oder sinkt.`

   - Wofür ein Kubernetes Service gut ist **(2 Punkte)**

   `Ein Kubernetes Service ist eine Abstraktion, die es erlaubt, auf eine Gruppe von Pods zuzugreifen. Ein Service definiert eine stabile IP-Adresse und einen Port, über die die Anwendung erreicht werden kann. Ein Service kann auch Load-Balancing und Discovery für die Pods bereitstellen.`

   - Mehrere Wege wie man eine Kubernetes Anwendung von außen erreichen kann **(3 Punkte)**

   `Eine Kubernetes Anwendung kann von außen erreicht werden, indem ein Service definiert wird, der die Anwendung bereitstellt. Ein Service kann vom Typ NodePort, LoadBalancer oder ClusterIP sein. Ein Service vom Typ NodePort stellt die Anwendung auf einem Port auf allen Nodes bereit. Ein Service vom Typ LoadBalancer stellt die Anwendung auf einem Port bereit und stellt sicher, dass der Traffic auf die Pods verteilt wird. Ein Service vom Typ ClusterIP stellt die Anwendung auf einem Port bereit und stellt sicher, dass der Traffic auf die Pods verteilt wird, aber nur innerhalb des Clusters.`

## Zusatzaufgabe:

Definiere einen Kubernetes Job **(2 Punkte)**
