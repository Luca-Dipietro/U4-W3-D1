Esercizio 1
SELECT *
FROM public."Clienti"
WHERE nome_cliente='Mario'

Esercizio 2
SELECT nome_cliente,cognome_cliente
FROM public."Clienti"
WHERE anno_nascita_cliente = 1982

Esercizio 3
SELECT numero_fattura
FROM public."Fatture"
WHERE iva_fattura = 20

Esercizio 4
SELECT *
FROM public."Prodotti"
WHERE EXTRACT(YEAR FROM data_attivazione_prodotto)= 2017
AND (inproduzione_prodotto = TRUE OR incommercio_prodotto = TRUE)
