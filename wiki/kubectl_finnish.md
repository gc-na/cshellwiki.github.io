# [Linux] Bash kubectl käyttö: Hallitse Kubernetes-klustereita

## Yleiskatsaus
`kubectl` on komentorivityökalu, jota käytetään Kubernetes-klustereiden hallintaan. Sen avulla voit luoda, muokata ja poistaa resursseja klusterissa, sekä tarkastella niiden tilaa ja lokitietoja.

## Käyttö
Perussyntaksi `kubectl`-komennolle on seuraava:

```
kubectl [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `get`: Hakee ja näyttää resursseja.
- `describe`: Näyttää yksityiskohtaisia tietoja resurssista.
- `create`: Luo uuden resurssin.
- `delete`: Poistaa olemassa olevan resurssin.
- `apply`: Soveltaa muutoksia resurssiin määritellyn konfiguraation perusteella.

## Yleiset esimerkit
- Hae kaikki podit:
  ```bash
  kubectl get pods
  ```

- Näytä tietoja tietystä podista:
  ```bash
  kubectl describe pod [podin_nimi]
  ```

- Luo uusi pod määrittelystä:
  ```bash
  kubectl create -f pod.yaml
  ```

- Poista tietty pod:
  ```bash
  kubectl delete pod [podin_nimi]
  ```

- Sovella muutoksia konfiguraatioon:
  ```bash
  kubectl apply -f config.yaml
  ```

## Vinkit
- Käytä `--namespace`-vaihtoehtoa, jos haluat työskennellä tietyssä nimessä.
- Hyödynnä `-o`-vaihtoehtoa tulostuksen muotoiluun, kuten JSON tai YAML.
- Tarkista komennot aina `kubectl --help` -komennolla, jos et ole varma käytöstä tai vaihtoehdoista.