# Lets-localize
h4 - A site, a site. My kingdom for a working local site! 

a) Tekstissään Susanna Lehto käy yksityiskohtaisesti läpi oman pilvipalvelimensa vuokraamisen ja sen perustamisen. Dokumentaatio on yksityiskohtaista ja hyvää asian tiimoilta.

b)  Susanna Lehto muodosti onnistuneesti command prompteilla palomuurin ja palomuuriin portin 22:lle aukon. Hän muisti myös päivittää palvelunsa.

   - Tekstissä olleet komennot: $ ssh root@(Tähän tulisi pilvipalvelun IP-osoite), sudo apt-get update, sudo apt-get install ufw, sudo ufw allow 22/tpc, sudo ufw enable
 
c) Susanna lisäsi onnistuneesti käyttäjätunnuksia, joilla hän tulisi hallitsemaan pilvipalvelimensa ympäristöä.
   Tässä kohtaa Susanna kohtasi haasteita ja alkoi analysoimaan sekä tekemään ongelmanratkaisua, mahdollisen syyllisen selvittämiseksi ja tilanteen ratkaisemiseksi.
   
  - Tekstissä olleet komennot: $ sudo adduser (käyttäjätunnus), sudo adduser (käyttäjätunnus) sudo, ssh (käyttäjätunnus)@(pilvipalvelimen palveluntarjoajan IP-osoite), sudo apt-get update, sudo usermod –lock root, ping           (sivunnimi).me
  - Ongelman ratkaisun käsittelyssa käytettyjä komentoja: 

d) Susanna lähestyi pilpipalvelimensa päivittämistä saamiensa ohjeiden mukaisesti ja ottaen huomioon että hänen palvelimelleen oltiin yritetty murtautua, oli päivitys erittäin hyvä toteuttaa.
  - Tekstissä olleet komennot: $ sudo apt-get update, sudo apt-get upgrade, sudo apt-get dist-upgrade, sudo less /var/log/auth.log | grep log, sudo less /var/log/auth.log | grep 10540

