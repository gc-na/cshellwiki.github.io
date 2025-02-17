# [Linux] Bash minikube käyttö: Kubernetesin paikallinen hallinta

## Yleiskatsaus
Minikube on työkalu, joka mahdollistaa Kubernetes-klusterin ajamisen paikallisesti. Se on erityisen hyödyllinen kehittäjille, jotka haluavat testata ja kehittää sovelluksiaan Kubernetes-ympäristössä ilman tarvetta käyttää suuria pilviresursseja.

## Käyttö
Minikubea käytetään komentoriviltä ja sen perussyntaksi on seuraava:

```bash
minikube [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `start`: Käynnistää Minikube-klusterin.
- `stop`: Pysäyttää Minikube-klusterin.
- `status`: Näyttää Minikube-klusterin tilan.
- `delete`: Poistaa Minikube-klusterin.
- `kubectl`: Suorittaa kubectl-komentoja Minikube-klusterissa.

## Yleiset esimerkit
### Klusterin käynnistäminen
```bash
minikube start
```

### Klusterin pysäyttäminen
```bash
minikube stop
```

### Klusterin tilan tarkistaminen
```bash
minikube status
```

### Klusterin poistaminen
```bash
minikube delete
```

### Kubectl-komentojen suorittaminen
```bash
minikube kubectl -- get pods
```

## Vinkit
- Varmista, että sinulla on tarpeeksi resursseja (muistia ja prosessoria) koneellasi ennen Minikuben käynnistämistä.
- Käytä `minikube dashboard` -komentoa avataksesi graafisen käyttöliittymän klusterin hallintaan.
- Hyödynnä Minikuben lisäosia, kuten `minikube addons`, lisätäksesi toiminnallisuuksia klusteriisi.