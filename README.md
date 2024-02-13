# Lets-localize
## h4 - A site, a site. My kingdom for a working local site! 
### Susanna Lehdon teksti ja sen läpikäyminen

a) Tekstissään Susanna Lehto käy yksityiskohtaisesti läpi oman pilvipalvelimensa vuokraamisen ja sen perustamisen. Dokumentaatio on yksityiskohtaista ja hyvää asian tiimoilta.

b)  Susanna Lehto muodosti onnistuneesti command prompteilla palomuurin ja palomuuriin portin 22:lle aukon. Hän muisti myös päivittää palvelunsa.

   - Tekstissä olleet komennot: $ ssh root@(Tähän tulisi pilvipalvelun IP-osoite), sudo apt-get update, sudo apt-get install ufw, sudo ufw allow 22/tpc, sudo ufw enable
 
c) Susanna lisäsi onnistuneesti käyttäjätunnuksia, joilla hän tulisi hallitsemaan pilvipalvelimensa ympäristöä.
   Tässä kohtaa Susanna kohtasi haasteita ja alkoi analysoimaan sekä tekemään ongelmanratkaisua, mahdollisen syyllisen selvittämiseksi ja tilanteen ratkaisemiseksi.
   
  - Tekstissä olleet komennot: $ sudo adduser (käyttäjätunnus), sudo adduser (käyttäjätunnus) sudo, ssh (käyttäjätunnus)@(pilvipalvelimen palveluntarjoajan IP-osoite), sudo apt-get update, sudo usermod –lock root, ping           (sivunnimi).me
  - Ongelman ratkaisun käsittelyssa käytettyjä komentoja: 

d) Susanna lähestyi pilpipalvelimensa päivittämistä saamiensa ohjeiden mukaisesti ja ottaen huomioon että hänen palvelimelleen oltiin yritetty murtautua, oli päivitys erittäin hyvä toteuttaa.
  - Tekstissä olleet komennot: $ sudo apt-get update, sudo apt-get upgrade, sudo apt-get dist-upgrade, sudo less /var/log/auth.log | grep log, sudo less /var/log/auth.log | grep 10540

### Oman virtuaalipalvelimen vuokraaminen tai ainakin sen yrittäminen

Aloitin menemällä GitHub Educationin ilmaiseksi tarjottavien palveluiden sivuille (https://education.github.com/pack/offers#namecom).

![GitHub Education](https://github.com/Andtonyk/h0/assets/149326156/c5e6b6b6-cf90-479c-99ea-0584b43fbaf2)

Täältä suuntasin DigitalOceaniin, sillä GitHubin kautta minulle piti olla mahdollisuus 200$ alkupanokselle.

DigitalOceanin perustamisessa oli sen alkuperäisen GitHub linkin kautta ongelmia. 

![DigitalOcean tilin hankkimisessa ongelmia](https://github.com/Andtonyk/h0/assets/149326156/08f2f399-fc85-4c82-9bf6-cd09b6789109)

Se onnistui vasta kun tajusin kirjautua palveluun suoraan DigitalOceanin pääsivun sisäänkirjautumisen kautta.

![DigitalOcean tilin onnistunut sisaankirjautuminen](https://github.com/Andtonyk/h0/assets/149326156/c7069b3b-abd3-4376-b754-300a6be56d57)

Perustin DigitalOceanin hyvin samoilla tiedoilla, kuin Susanna Lehto omassa esimerkissään.

Tein vahvat salasanat, en ottanut lisäpalveluita.

Perustamisen jälkeen minulla oli pilvipalvelu, jossa oli vahva salasana ja jonka kontaktipalvelimet sijaitsivat Amsterdamissa.

### Domain, valitsen sinut... tai ainakin yritän

Aloitin yrityksen GitHUb Educationin vaihtoehdolla Name.comin tarjousta ilmaisesta palvelusta.

Kyseisen palvelun onnistuneen käyttöönoton kanssa oli isoja ongelmia. Yritetään jotain toista vaihtoehtoa.

Kokeillaan vaihtoehtoa Namecheap.

Namecheap oletuksellisen ongelmatilan jälkeen perusti tunnukseni onnistuneesti.

Tämän jälkeen etenin Domain listiin ja sieltä Advanced DNS-valikkoon. Advanced DNS:ssä perustin uudet DNS:st, jotka pohjautuvat DigitalOceanista saamaani IP-polkuun

![digitalocean dns](https://github.com/Andtonyk/h0/assets/149326156/856edfaa-9220-4fd2-9dc1-9b96ef63d0d3)


### Debian asetuksien muokkaaminen ja toteuttaminen


