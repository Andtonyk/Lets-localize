Huom! Kaikki testit on toteuttu seuraavanlaisella koneella: Windows 10 OS:llä, Google Chrome selaimella ja koneena on toiminut Legion 5 kannettava. 16Gt RAM, AMD Ryzen 7 5800H, NVIDIA Geforce 3070 ja 200GB vapaata levytilaa SSD-levyasemalla.

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

Valitsin paketin ja sen suojaus metodin.


Sain itselleni domainin andreask.me

Tämän jälkeen etenin Domain listiin ja sieltä Advanced DNS-valikkoon. Advanced DNS:ssä perustin uudet DNS:st, jotka pohjautuvat DigitalOceanista saamaani IP-polkuun

![digitalocean dns](https://github.com/Andtonyk/h0/assets/149326156/856edfaa-9220-4fd2-9dc1-9b96ef63d0d3)


### Debian asetuksien muokkaaminen ja toteuttaminen

Aloitin avaamalla aiemmin muodostaneeni VM:n ja siellä terminalin.

Kirjauiduin normaalistakäyttäjätunnuksestani domainista vastaaville tunnuksille.

![ssh root sisaankirjautuminen](https://github.com/Andtonyk/h1---Debian/assets/149326156/97ed3d29-724f-44d7-b5f0-8099a8cbee3e)

Kirjautumisen jälkeen asetin päivitykset domainista vastaavalle palvelimelle.

![kayttajan tilin paivitykset toteutettu](https://github.com/Andtonyk/h1---Debian/assets/149326156/fa1424c7-b8ba-4e2a-9a46-062515c74206)

Päivityksien jälkeen suljin rootin.

![root lukittu](https://github.com/Andtonyk/h1---Debian/assets/149326156/cd353aca-d9d9-4882-94d5-839cd4252f9c)

Muodostin tämän jälkeen uuden käyttäjän...

![kayttajan lisays](https://github.com/Andtonyk/h1---Debian/assets/149326156/20fff288-3e36-4bab-b5c2-ce3861c9c376)

...Sekä päivitin käyttäjää koskevat asetukset.

![kayttajan tilin paivitykset toteutettu](https://github.com/Andtonyk/h1---Debian/assets/149326156/2e18c7fe-8d04-4b9c-9554-c7ecc21c3076)

Muodostin tämän jälkeen portillisia poikkeuksia palomuuriin.

![portti 80 aktiivisena](https://github.com/Andtonyk/h1---Debian/assets/149326156/7500c423-f1f1-4f7e-844c-7e2be213cec5)

![portti 443 on auki](https://github.com/Andtonyk/h1---Debian/assets/149326156/c19bfad7-f5e8-4d6f-8b88-5a86c7ac4b35)

Testasin samalla pyös pingauksella sivujen tilan, ennen kuin uskaltauduin selain näkymään.

![ping testattu andreask me ja toimii](https://github.com/Andtonyk/h1---Debian/assets/149326156/d9a7e8a5-5d00-41cb-a19a-2be255232ee6)

Sivut toimivat! Niin DNS-haulla kuin suoraan IP-osooitteella haettaessa.

![andreask me saa myos debian nakyman](https://github.com/Andtonyk/h1---Debian/assets/149326156/a0a39665-4626-4b9f-8648-0a69328fe81e)

![Apache2 Debian sivu nakyy ipssa 157 245 72 185](https://github.com/Andtonyk/h1---Debian/assets/149326156/d5cbb31d-6cad-47e9-bdcd-1dfc07a1517f)
