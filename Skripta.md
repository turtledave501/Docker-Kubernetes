# Docker a Kubernetes: Úvodní Průvodce

Tento dokument slouží jako rychlý úvod pro práci s kontejnery a orchestrací pomocí Dockeru a Kubernetes. Poskytuje základní informace a ukazuje první kroky pro začínající uživatele.

## Docker: Efektivní kontejnerizace

### Co je to Docker?
Docker je výkonná platforma pro vytváření, distribuci a spouštění aplikací v kontejnerech. Kontejnery umožňují balit aplikace spolu se vším potřebným do lehkých, přenosných balíčků. Tyto balíčky lze poté snadno nasadit a spustit kdekoli, kde je dostupný Docker, a to s garantovanou konzistencí prostředí.

### Instalace Dockeru
Přejděte na oficiální stránky a stáhněte Docker pro váš operační systém:

[Docker: Stránka pro stažení](https://www.docker.com/get-started/)

### Základní pojmy v Dockeru
- **Obraz (Image)**: Statická definice aplikace a jejích závislostí.
- **Kontejner (Container)**: Běžící instance obrazu, která poskytuje izolované prostředí pro aplikace.

### Nezbytné příkazy Dockeru

#### Stažení obrazu z registru
```bash
docker pull nazev_obrazu
```

#### Spuštění kontejneru z obrazu
```bash
docker run nazev_obrazu
```

#### Výpis aktivních kontejnerů
```bash
docker ps
```

#### Zastavení kontejneru
```bash
docker stop id_kontejneru
```

## Kubernetes: Automatizace nasazování kontejnerů

### Co to je Kubernetes?
Kubernetes, známý také jako K8s, je open-source systém pro automatizovanou správu, škálování a orchestraci kontejnerizovaných aplikací. Platforma usnadňuje správu aplikací běžících ve více kontejnerech a optimalizuje jejich spuštění v cloudu nebo na lokálních serverech.

### Základní koncepty Kubernetes
- **Pod**: Základní spustitelná jednotka, může obsahovat jeden nebo více těsně propojených kontejnerů.
- **ReplicaSet**: Udržuje požadovaný počet kopií podu v běhu.
- **Deployment**: Správa verzí a nasazení aplikací, automatická aktualizace a rollback.
- **Service**: Abstrakce, která poskytuje síťovou identitu podům a umožňuje jejich vzájemnou komunikaci.

## Jak začít s Dockerem

### 1. Nastavení Dockeru

#### Windows
Stáhněte Docker Desktop z odkazu [Docker Desktop pro Windows](https://www.docker.com/products/docker-desktop) a postupujte podle pokynů k instalaci.

#### macOS
Navštivte [Docker Desktop pro macOS](https://www.docker.com/products/docker-desktop) a stáhněte si aplikaci Docker.

#### Linux
Pro instalaci Dockeru na Linuxu použijte příkazy odpovídající vaší distribuci. Pro Ubuntu může postup vypadat takto:
```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### 2. První kroky s Dockerem

Po instalaci Dockeru můžete začít experimentovat s kontejnery:

#### 1. Stáhněte obraz z Docker Hubu
```bash
docker pull hello-world
```

#### 2. Spusťte svůj první kontejner
```bash
docker run hello-world
```
To vytvoří a spustí kontejner z obrazu `hello-world`, což je jednoduchá demonstrační aplikace.

### 3. Přístup k aplikaci
Prostřednictvím příkazu `docker run` můžete spustit kontejnery s webovými aplikacemi a přistupovat k nim pomocí webového prohlížeče na určeném portu.

#### Příklad:
```bash
docker run -p 8080:80 nazev_webove_aplikace
```
Poté můžete aplikaci navštívit na `http://localhost:8080`.

### Souhrn
S Dockerem můžete snadno začít vytvářet a spravovat kontejnery pro vaše aplikace. Další informace a pokyny pro pokročilé konfigurace najdete v [oficiální dokumentaci Dockeru](https://docs.docker.com/).

Pro zájemce o Kubernetes doporučujeme pokračovat vzděláním prostřednictvím [oficiální dokumentace Kubernetes](https://kubernetes.io/docs/home/), kde naleznete detailnější informace a postupy pro práci s tímto nástrojem.
