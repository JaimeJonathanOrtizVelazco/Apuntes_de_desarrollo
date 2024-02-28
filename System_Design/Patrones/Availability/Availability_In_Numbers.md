# Disponibilidad en numeros

Normalmente la disponibilidad es cuantificable en terminos cuanto tiempo el servicio se encuentra funcionando.

Los criterios para 3 9s son:
Duration | Acceptable downtime
------------- | -------------
Downtime per year | 8h 41min 38s
Downtime per month | 43m 28s
Downtime per week | 10m 4.8s
Downtime per day | 1m 26s

Mientras que los criterios para 4 9s son
Duration | Acceptable downtime
------------- | -------------
Downtime per year | 52min 9.8s
Downtime per month | 4m 21s
Downtime per week | 1m 0.5s
Downtime per day | 8.6s

La disponibilidad en paralelo y secuencia se calculan de la siguiente manera

## Secuencial

`Availability (Total) = Availability (Foo) * Availability (Bar)
`

## Paralelo

`Availability (Total) = 1 - (1 - Availability (Foo)) * (1 - Availability (Bar))
`
