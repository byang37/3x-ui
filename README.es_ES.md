# 3X-UI Fork: multiplicador de tráfico

Este repositorio es un fork personal de 3X-UI. Sigue el proyecto upstream y este README se centra solo en las funciones principales agregadas fuera del upstream.

## Función principal agregada

### Multiplicador de tráfico para inbound

Este fork agrega un multiplicador de tráfico para los nodos inbound.

- Los formularios Add Inbound y Edit Inbound incluyen un campo Traffic Multiplier.
- El valor predeterminado es `1`, lo que mantiene el comportamiento original de conteo de tráfico.
- Si el multiplicador se configura en `2`, el upload y download del inbound se contabilizan como el doble del uso real.
- El upload y download de cada client dentro del inbound también se contabiliza con el multiplicador.
- El tráfico restante del client y las comprobaciones de límite usan los valores ponderados.
- La sincronización de inbound con remote nodes incluye el valor del multiplicador.
- Los subscription links no cambian. El uso y el tráfico restante en la subscription se basan en los contadores ponderados de client.

## Instalar este fork

```bash
bash <(curl -Ls https://raw.githubusercontent.com/byang37/3x-ui/master/install.sh)
```

## Referencia upstream

Este fork se basa en el proyecto upstream:

[MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)
