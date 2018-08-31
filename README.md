# SPI
Generate forecast vidéo 

1) use group account on ppp (so A & P have access):
ssh -XC sdfo500@eccc-ppp2

2) the project is in the directory
cd ~/SeDOO/requests/CCG/Gulf_of_Gothia/sample

3) Open SPI
SPI
Files/open_project : CCG_Gulf_of_Gothia.spi

4) Aller chercher les produits opérationnels (dans ce cas si - RIOPS pour Océan Artique) 
cd $CMCGRIDF/prog/riops.native
Files/open : files of the last run of forecasts (ex. next 48 hours)

ouvrir la console et inscrire : fstdfield vector { UUW VVW }




