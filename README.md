# Prosjektnavn
REST-basert API som eksponerer forretningslogikk for xxx-portal, bygget på .NET Core 2.1.
 
# Oppstart
Utvikling krever Visual Studio 2018 v15 eller nyere
Database er MSSQL 2017. MSSQL 2017 kan lastes ned fra https://www.microsoft.com/en-au/sql-server/sql-server-downloads *OBS*: Må installeres med kombinert Windows og passord-security. Oppdater denne guiden om du møter på problemer som ikke er dokumentert her.

# Arkitektur
1.	[Applikasjonsarkitektur] (https://lenke.til.arkitektur.com) (lenke til confluence/sharepoint e.l)
2. [Driftsarkitektur] (https://lenke.til.arkitektur.com)  (lenke til confluence/sharepoint e.l)

# Kjør løsningen lokalt
1. Klon dette repoet: `https://github.com/JoachimL/AdcEksempelrepo.git`
2. Bygg løsningen src\AdcEksempel\AdcEksempel.sln
3. Opprett lokale databaser (høyreklikk database-prosjektene og velg "Publish")

# Bygg og testing
Utviklingmetodikken er basert på TDD, slik at vi skriver tester før produksjonskode. 
For å ivareta kodekvalitet brukes Stylecop med eget definert regelsett, samt hyppig codereviews.
Ved opprettelse av pullrequest gjøres det en automatisk sjekk av kodekvalitet, alle enhestester kjøres og det gjøres
en release til ST hvor alle Atestene kjøres. 

# Fra utvikling til produksjon
En oppgave testes alltid av utvikler i testmiljø før den assignes til tester i Trello/TFS/Jira. Tester merger deretter koden til master, og kjører dette i produksjon.
