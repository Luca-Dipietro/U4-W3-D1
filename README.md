Esercizio 1
SELECT *
FROM clienti
WHERE nome_cliente='Mario'

Esercizio 2
SELECT nome_cliente,cognome_cliente
FROM clienti
WHERE anno_nascita_cliente = 1982

Esercizio 3
SELECT iva_fattura, COUNT(*)
FROM fatture
WHERE iva_fattura = 20 GROUP BY iva_fattura

Esercizio 4
SELECT *
FROM prodotti
WHERE EXTRACT(YEAR FROM data_attivazione_prodotto)= 2017
AND (inproduzione_prodotto = TRUE OR incommercio_prodotto = TRUE)

Esercizio 5
SELECT *
FROM fatture
JOIN clienti ON fatture.id_cliente = clienti.numero_cliente
WHERE fatture.importo_fattura < 1000

Esercizio 6
SELECT numero_fattura,importo_fattura,iva_fattura,data_fattura,nome_cliente
FROM fatture
JOIN clienti ON fatture.id_cliente = clienti.numero_cliente

Esercizio 7
SELECT EXTRACT (YEAR FROM data_fattura) , COUNT(*) 
FROM fatture where iva_fattura = 20 GROUP BY data_fattura
